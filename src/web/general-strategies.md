# Web - General Strategies
These are some general strategies when tackling web problems

## 1. Source Files
Analyizing source files is incredibly important. Here are some common things you should look out for.
To get the source files take a look at the source tab in DevTools.

![css file contains part of flag](https://user-images.githubusercontent.com/58456527/224190440-9a759a89-48ca-4fa0-b316-616997b6994f.png)

### Comments
```html
<body>
  <div>
    <p>Welcome to my website!</p>
    <!-- pst, the hidden page is at /7dj4Dk.html -->
  </div>
</body>
```
Sometimes important parts of the challenge will be hidden in comments. These can be find in html, css and js files.

#### Practice
* [picoCTF: Insp3ct0r](https://play.picoctf.org/practice/challenge/18?category=1&page=1) [(Direct Link)](https://jupiter.challenges.picoctf.org/problem/44924/)

### Client Side Javascript
```js
function validatePassword(password) {
  if (btoa(password) == "ZmxhZ3t0aGlzXzEkX3RoM19mbGFnfQ==") {
    alert("Password verified");
  } else {
    alert("Password is wrong");
  }
}
```
Websites should not validate sensitive information like passwords on the client side. If a question does this, you can look at the javascript to see how they validate the data, then attack it.

#### Practice
* [picoCTF: dont-use-client-side](https://play.picoctf.org/practice/challenge/66?category=1&page=1) [(Direct Link)](https://jupiter.challenges.picoctf.org/problem/29835/)

### .well_known
```
User-agent: *
Disallow: /users/admin
```
Some challanges will have some `.well_known` files. The most famous being (robots.txt)[http://www.robotstxt.org/]. Looking at these files might provide you with crucial information.

#### Practice
* [picoCTF: where are the robots](https://play.picoctf.org/practice/challenge/4?category=1&page=1) [(Direct Link)](https://jupiter.challenges.picoctf.org/problem/60915/)

## 2. Servers

### Cookies
When requesting a website, sometimes servers will return cookies and your browser will set them. You can sometimes edit these cookies to trick the server into believing something.

#### Practice
* [picoCTF: logon](https://play.picoctf.org/practice/challenge/46?category=1&page=1) [(Direct Link)](https://jupiter.challenges.picoctf.org/problem/15796/)
