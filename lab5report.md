# Lab Report 5

## Part 1

The following debugging scenario is loosely inspired by my personal experience in a lab earlier this quarter.

### A student makes the following private EdStem post regarding running tests for `ListExamples.java`:

Hello, I am really confused as to why my test.sh bash script isn't working. I am trying to run JUnit tests in `ListExamplesTests.java` to test the provided implementation of `filter()` and `merge()` in `ListExamples.java`, with the following directory structure:

![](Post1_Files.png)

Here is the bash script I am working with:

![](Post1_Bash.png)

Here is the output I get when I try to run it:

![](Post1_Error.png)

Here is what I have tried to debug the scenario. The error says "java.lang.IllegalArgumentException: Could not find class [src/ListExamplesTests]" so the first thing I thought of was to check if the file src/ListExamples even exists. I did by checking if the file is listed when I do `ls` and if I can cat the file and get some confirmation of the file containing something:

![](Post1_Attempt.png)
![](Post1_Exists.png)

Knowing the file exists, and that `cat` can reach it, I tried running `java src/ListExamples` hoping to get some confirmation of the file existing, but instead got this:

![](Post1_Identification.png)

I'm very confused; how can other bash commands like `ls` or `cat` tell me something exists at that path, but `java` could not? Could course staff please help?

### A TA writes the following response:

The issue you're experiencing is less of a mistake on your part, but a limitation of the `java` command.
Try `cd` into `src` and compiling and running the tests from there, directly calling the file name rather than its relative path from your main directory.
What do you notice? Do the errors still persist? What specifically did you change by moving into the `src` directory?
Think about what you changed, and how this might be related to how `java` interprets relative paths, or paths in general.

### The student gives the following response:

Thank you for the quick response. You're right, when I `cd src` and try to run `java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`, changing both the classpath (by adding `../` to the start of both paths) and the path of the file to be run (from `src/ListExamplesTests` to `/ListExamplesTests`) I get a successful test run:

![](Post2_Success.png)
