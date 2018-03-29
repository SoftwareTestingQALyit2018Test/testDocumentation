<link rel="stylesheet" href="prism.css">
<script src="prism.js"></script>

<style>body { padding: 20px } pre { padding: 0 }</style>


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


```shell
$ vim helloWorld.java
...
$
```

Where `vim` is a well known text-editor which is invoked with a single argument
which the name of the Java source code.

`helloworld.java` is the SUT element in this testing example and is very simple in
its behaviour:


<pre ><code class="language-java line-numbers"> 
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
