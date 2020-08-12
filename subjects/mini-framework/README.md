## mini-framework

Now that you have already used a framework of your choice, you must now implement some features on a framework of your own. That's right, you are going to create a framework.

Be aware that a framework is different from a library. When you call a method from a library, you are in control. But with a framework, the control is inverted: the framework calls you.

### Objectives

Your framework should implement:

- Abstracting DOM
- Easier Routing
- State Management
- Event Handling

### Instructions

Your framework will be tested by using it, like you previously have used one, in the social network project. So the user has to be presented to a folder structure that when executed `npm start` at the root of the folder, it runs the app. The user testing your framework will have to implement some simple code in order to test the features described bellow.

#### Abstracting DOM

You will have to implement a way to handle the DOM. The DOM can be seen as a big object, like in the example below:

```html
<html>
  <div class="nameSubm">
    <input type="text" placeholder="Insert Name" />
    <input type="submit" placeholder="Submit" />
  </div>
</html>
```

The html above can be written as:

```json
{
  "tag": "html",
  "attrs": {},
  "children": [
    {
      "tag": "div",
      "attrs": {
        "class": "nameSubm"
      },
      "children": [
        {
          "tag": "input",
          "attrs": {
            "type": "text",
            "placeholder": "Insert Name"
          }
        }, //</input>
        {
          "tag": "input",
          "attrs": {
            "type": "submit",
            "placeholder": "Submit"
          }
        } //</input>
      ]
    } //</div>
  ]
} //</html>
```

With this in mind you can manipulate the DOM more easily in JS. And that is what you will do using a method. Here are some methods you can use:

- [Virtual DOM](https://bitsofco.de/understanding-the-virtual-dom/) - Using a second DOM with the wanted changes, to compare with the real DOM and change just what is needed
- [Data Binding](https://docs.microsoft.com/en-us/dotnet/desktop-wpf/data/data-binding-overview?redirectedfrom=MSDN) - binds together two data sources and keeps them synchronized
- [Templating](https://medium.com/@BuildMySite1/javascript-templating-what-is-templating-7ff49d97db6b) - refers to the client side data binding method implemented with the JavaScript language.

There are a lot of ways to achieve this. Above are just some examples, what matters is that the DOM must respond to certain actions of the user.

---

#### Easier Routing

Routing is the process of selecting a path for traffic in a network. And, as you may have already realized, routing in JS can sometimes be a little bit confusing, so what you will need to do, is to implement a new routing system that is more intuitive and simpler.

Also take in consideration that all kind of URLs must be supported, like for example queries in the URL from GET requests (example: `http://something.com/users?id=31&tkn=31inasdasni213n1i23ni213ojo`) or not found pages.

---

#### State Management

The state of an app can be seen as the outcome of all of the actions that the user has taken since the page loaded. In other words, if a user clicks on a button to execute an action, the state should then change.\
What you will need to do is to implement a way to handle this state. Remember that multiple pages can need to interact with the same state, so you need to find a way to let the state be reachable at every time.

---

#### Event Handling

You will also have to implement a way to handle the events triggered by the user, like: scrolling, clicking, certain keybindings, etc.... Note that this new way of handling events must different from the `addEventListener()` method that already exists.

---

This project will help you learn about:

- Web Development
- Frameworks
- DOM
- Routing
- State of an Application