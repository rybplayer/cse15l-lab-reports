# Lab Report 1

## Part 1: String Server

Here is the code I wrote for the specified server:
![ServerCode.png](ServerCode.png)

Here is what the server looks like when starting up:
![ServerStart.png](ServerStart.png)

Here I add the string `Hi` using `\add-message` request:
![ServerAdd1.png](ServerAdd1.png)
1. The method `handleRequest` is called.
2. The method takes in the URL as an argument, and then modifies the addedList field.
3. In the first screenshot, by accessing the root URL I effectively call handleRequest() setting argument `url="/"`. This triggers the first case, returning the ArrayList<String> `addedList` conactenated, sepaarted by newline characters, into one String called `result`. This is printed on the screen as nothing, as `result` is initialized to be the empty string. \
In the second screenshot, I effectively call handleRequest() again, this time setting argument `url=/add-message?s=Hello`. This causes `parameter=["s","Hello"]`, which passes the if statement adding `"Hello"` to the end of the `addedList` ArrayList<String> using .add(). Then the String `"String Hello added!"` is returned and printed on the screen.\

The result is as follows:
![ServerResult1.png](ServerResult1.png)

Here I add the string `Hello` using `\add-message` again:
![ServerAdd2.png](ServerAdd2.png)
1. The method `handleRequest` is called.
2. The method takes in the URL as an argument, and then modifies the addedList field.
3. In the third screenshot, by accessing the root URL I effectively call handleRequest() setting argument `url="/"`. This triggers the first case, returning the ArrayList<String> `addedList` conactenated, sepaarted by newline characters, into one String called `result`. This is printed on the screen. \
In the fourth screenshot, I effectively call handleRequest() again, this time setting argument `url=/add-message?s=Hi`. This causes `parameter=["s","Hi"]`, which passes the if statement adding `"Hi"` to the end of the `addedList` ArrayList<String> using .add(). Then the String `"String Hi added!"` is returned and printed on the screen.\
The final screenshot shows the same process as the first screenshot, but this time as `addedList` has one more element, one more line is printed out.

The result is as follows:
![ServerAddResult.png](ServerResult2.png)

## Part 2

The screenshot below shows is the path to my private SSH key for logging into ieng6 I found with `ls`. \
The path is `/.ssh/id_rsa.pub`, as using `cat` on it prints out my RSA key.
![TerminalPrivate.png](TerminalPrivate.png)

The screenshot below shows the path to my public SSH key for logging into ieng6 in my account I found on ieng6 with `ls`. \
The path is `/.ssh/authorized keys`, as using `cat` on it prints out my RSA key.
![TerminalPublic.png](TerminalPublic.png)

Here is me logging into my ieng6 account without being asked a password:
![TerminalLogin.png](TerminalLogin.png)

## Part 3

One thing I learned a lot about from Week 2 was making web servers in Java. \
I learned the basics of how to parse a url into requests in Java, as well as what happens when this breaks down. \
In addition, I learned a bit about what ports mean and why compiling `java NumberServer.java 4000` does not work if something is already using port 4000.
