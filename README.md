# 🎮 Picking Up Carrots Game

This is one of the toy projects made with **Vanilla JavaScript** without any framework. It includes very basic yet important front-end features.

## 🔍 Project description

🥕 Users win when they

- click all the carrots before time is up

🪰 Users lose when they

- click any bug or
- fail to click all the carrots within the time limit

## 🔨 Note

### ❗️

In an attempt to do refactoring by creating js modules...

- you need to include `type="module"` in the `<script>` element, to declare this script as a module
- for example: to import the `main.js` script, we use this:

```
<script type="module" src="main.js"></script>
```

During this process, you might run into an error in local testing environment 🤦🏻‍♀️

- if you try to load the HTML file locally (i.e. with a `file://` URL), you'll run into CORS errors due to JavaScript module security requirements.
- You need to do your testing through a server. [MORE INFO HERE](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
- ✨ SOLUTION ✨ : (if you use VS Code) INSTALL [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension
