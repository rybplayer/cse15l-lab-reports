CSE15L FA23 Lab 1
Example Markdown file.

We can use *italics* to slightly emphasize something.
Alternatively **bold** to really emphasize something.

# If it's important enough it could become a heading
## Or even a subheading

We can also link other files or sites like [Joe's](https://jpolitz.github.io/cse-15l-lab-report/index.html)
Or add images like ![Image](http://url/favicon.png)

We could also quote something long:
> The .md extension stands for “Markdown,” which is a particular text format used for writing. 
> There are many good documents on the web. 
> A good cheat sheet and explainer are here:

Alternatively we could format a list of markdown features:
* Italics
* Bold
* Headings

If we want to start something new, consider adding a horizontal rule:
---

We could also quote some code inline like 'javac Hello.java'
Alternatively we could have multiline code blocks for entire files, like:
```
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}
```
