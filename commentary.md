
<link rel="stylesheet" href="pandoc.css">
<link rel="stylesheet" href="prism.css">
<script src="prism.js"></script>

<style>body { padding: 150px } pre { padding: 0 }</style>


# Commentary on Example 1

## Synopsis
The purpose of the example is to show the bare bones invocation of a JUnit test
from the command line and then provide a detailed commentary on the elementary
steps in the JUnit testing process.


In this example we have a Java source file which contains a SUT, a system
under test, and an accompanying JUnit 4 test.


## The System Under Test
The first step is to create the SUT - in this simple example I will create and
execute all commands from a bash shell:



<pre class="command-line" data-user="martin" data-host="localhost" data-output="2, 4-8"><code class="language-bash">
$ vim helloWorld.java
...
$
</code> </pre>

Where `vim` is a well known text-editor which is invoked with a single argument
which the name of the Java source code.

`helloworld.java` is the SUT element in this testing example and is very simple in
its behaviour:


<pre class="line-numbers"><code class="language-java" >
import java.io.*;

public class helloWorld{

    private String name;

	public String sayHello(){
		return("Hello");
	}

	public String sayGoodbye(){
		return ("Goodbye");
	}

    public String sayName(String name){
        this.name = name;
        return name;
    }
}
</code></pre>

And then we have this command line output:
<pre class="command-line" data-user="martin" data-host="localhost" data-output="2, 4-8"><code class="language-bash">
pwd
/usr/home/martin/bin
ls -la
total 2
drwxr-xr-x   2 chris  chris     11 Jan 10 16:48 .
drwxr--r-x  45 chris  chris     92 Feb 14 11:10 ..
-rwxr-xr-x   1 chris  chris    444 Aug 25  2013 backup
-rwxr-xr-x   1 chris  chris    642 Jan 17 14:42 deploy
</code></pre>


<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
