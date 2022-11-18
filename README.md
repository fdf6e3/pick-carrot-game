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

### ❗️❗️

In an attempt to do refactoring by creating js modules...

- you will encounter bugs unless you bind methods in classes [MORE INFO HERE](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- there are three ways to bind functions

```
1.
// Add .bind() method
this.onClick = this.onClick.bind(this)

2.
// Use an Arrow function syntax 1
// from this
this.field.addEventListener('click', this.onClick);
// to this
this.field.addEventListner('click', (event) => this.onClick(event));

3.
// Use an Arrow function syntax 2
onClick = event => {
  const target = event.target;
  if (target.matches('.carrot')) {
    target.remove();
    sound.playCarrot();
    this.onItemClick && this.onItemClick('carrot');
  } else if (target.matches('.bug')) {
    this.onItemClick && this.onItemClick('bug');
  }
};

```

- and I decided to bind the function in the class properties by using an arrow function syntax(like 3. above) since it is also an applicable way in using React

```
	// from this
	onClick (event) {
		// onClick logics
	};
	// to this ✨
	onClick = (event) => {
		// onClick logics
	};
```

### ❗️❗️❗️

In an attempt to do refactoring...

- you can implement a builder pattern like [this](https://github.com/younghyun-bae/pick-carrot-game/commit/fec4cbee0e96005e20b4f54a074d90190794cf11) in the project.
- a builder pattern separates the construction of a complex object from its representation.
- by implementing a builder pattern, you can build a complex object using simple object.
