# PreventCrossSiteScripting

So we have talked about what cross site scripting is and how to perform cross site scripting so now let’s talk about how to prevent it. This is actually easier than you may think. Most cross site scripting is caused because a developer accidentally renders user inputted information as HTML on the page. In JavaScript this is as easy as using innerHTML to render content on a page. If any of the content inside the innerHTML is provided by a user then you are vulnerable to cross site scripting.

The easiest way to fix this issue is to use innerText instead of innerHTML since innerText will convert all input into a string and will never render any of the values as HTML. If you really need to use innerHTML, though, you can use sanitization in order to convert the user input from HTML into a normal string by escaping all HTML specific characters. There are plenty of libraries that can do this for you.

In general I recommend not using innerHTML unless you specifically know that no user input will be used within it since it leads to easy cross site scripting vulnerabilities. By just changing from innerHTML to innerText we can fix the previous cross site scripting example. Here is what an example of using innerText would look like.

![image](https://github.com/derryderajat/PreventCrossSiteScripting/assets/38938185/57b0b430-6320-45ca-ba34-df3a16301be0)

thanks for
**webdevsimplified**
