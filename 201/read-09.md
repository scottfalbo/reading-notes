## 201 Read-09: Forms and JS Events
[jump to Styling list, tables and forms](#styling-lists-tables-and-forms)<br>
[jump to JavaScript Events](#events)

### Forms
*Duckett html and css chapter 7 pages 144-175*

**Form Controls**
+ Adding Text
  + **text input**: A single line input
  + **password input**: A single line that masks characters
  + **text area**: A longer area of text for messages
+ Making Choices
  + **radio buttons**: Used to select one choice out of multiple.
  + **checkboxes**: Can select and unselect multiple options.
  + **drop-down boxes**: Used to give options in list form.
+ Submitting Forms
  + **submit buttons**: Submits data from yur form to another page.
  + **image button**: Same as above with an image.
+ Uploading Files
  + **file upload**: Allows user to upload photos to the site.

**How it works**
1. The user fills out a form and presses a button to submit the information to the server.
2. The name of the form control as well as the values are sent to the server. 
3. The server processes the information.  it may also store it in a database.
4. Then the server creates a new page to send back to the browser based on the information.

Information is sent to the server using name/value pairs
+ `username = spaceghost`
  + `name = value`

#### Form Structure
+ The form control lives inside of the `<form>` element.
  + Every `<form>` element requires an **action attribute**.  It's value is the URL for the page that will receive the information.
  + `<forms>` also carry a **method attribute**.  There are two methods, `get` and `post`.
    + `get` is best used for short forms like search boxes or if you are just receiving data from the server.
    + `post` method sends the values as **HTML Headers** and should be the implemented method.
      + allows users to upload files
      + if its a very long form
      + contains sensitive material, passwords
      + adds information to, or deletes from a database
  + Forms also have an **ID attribute** that can be used to identify it distinctly.

*Duckett html and css pages 152-162 for input* `types`

#### labeling Form Controls

+ Each form control should have its own `<label>` element to make the form accessible to page readers.
  + There are two ways to use the `label` element.
    + You can wrap both the text description and input form in the tag.
    + `<label>SomeInput: <input type="text" name="someInput" /></label>`
    + or, it can be kept separate and use the `for` attribute
    + ```
      <input id="formName" type="text" name="someInput">
      <label for="formName">SomeInput</label>
      ```
    + Using the `for`and `id` attributes to label inputs increases the clickable area for radio buttons and check boxes.
  + Best placement for labels on form controls
    + Above and to the left
      + text input, text area, select boxes, file uploads
    + To the right
      + individual checkboxes
      + individual radio buttons

`<fieldset>` and `<legend>` are used to group and identify related forms

*Duckett html and css pages 165-168, Form validation, date input, email and url input and search input*.

> Any form can have a placeholder text by using the `placeholder` attribute in the input element.


### Styling Lists, Tables and Forms
*Duckett html and css chapter 14 pages 330-357*

`list-style-type` property
+ `<ul>` can use `none, disc, circle, square`
+ `<ol>` can use `decimal, decimal-leading-zero, lower-alpha, upper-alpha, lower-roman, upper-roman`
  + ```
    ol {
      list-style-type: upper-alpha;
    }
    ```
+ `list-style-image: url("images/file.png");` can be used to insert an image as a bullet point.
    + this can used in the `<ul>` or `<li>` elements

+ `list-style-position: outside/inside;`
  + This places the bullet either outside or inside of the block of text.

**List Style Shorthand**
  + `list-style: inside circle;` would assign both position and type

*Duckett html and css pages 337-346 table and form styling attributes, pretty much the same as any other.*

**Unique attributes**
+ Empty Cell: `empty-cells: show/hide;` hides or shows empty cells
+ Collapse: `border-collapse: collapse;`
  + Borders are collapsed to a single border where possible.  `border-spacing` and `empty-cells` are ignored.
+ Focus and Hover: `input:focus, input:hover`
  + Hover takes effect when the mouse cursor is over the element
  + Focus changes the color when it's being used
+ Cursor Styles: `cursor: default;`
  + `auto, crosshair, default, pointer, move, text, wait, help, url("some.gif")`
    + use cursor types where they are relevant so its not confusing to the user.


### Events
*Duckett javascript chapter 6 pages 243-292*

> Different events occur in the browser while you are browsing the web.  Any of these events can be used to trigger a function in your JavaScript.
+ UI events
+ Keyboard events
+ Mouse events
+ Focus events
+ Form events
+ Mutation events
  + *Duckett javascript pages 246-247 for a list of events*

When an event occurs it has been **Fired** or **Raised** and this will cause it to **Trigger** a function or script.

+ There are three parts involved in triggering code, these steps are referred to as an **Event Handler**
  + Select the element node(s) you want the script to respond to.
  + Indicate which **event** on the selected node(s) will trigger the response.
    + this is known as **Binding** an event to a DOM node.
  + State the code you want to run when this event occurs.

There are three types of **Event Handlers**
+ **HTML event handlers** *Bad practice, don't do it*
+ **Traditional DOM event handlers**
  + > All modern browsers understand this way of creating an event handler, but you can only attach one function to each event handler.
  + `elementNode.*on*event = functionName;`
  + ```
    function someFunction(){
      // do some stuff
    }
    var element = document.getElementById('someName');
    element.onclick = someFunction;
    ```
    + The `()` are omitted in the event handler so the code does not run until fired.
+ **DOM level 2 event listeners**
  + Event listeners are a more modern approach.  They can handle more than one function at a time.
    + `element.addEventListener('event', functionName, boolean);`
    + adapting the above code snippet the last line would instead be:
      + `element.addEventListener('click', someFunction, false);`
      + The boolean at the end controls event flow, more to follow.

+ Parameters and Event Handlers
  + Because you cannot use `()` in even handlers you have to use a work around to pass parameters in.
    + ```
      element.addEventListener('click', function() {
        someFunction(parameter);
      }, false;
      ```

#### Event Flow
> HTML elements nest inside other elements.  If you hover or click on a link, you will also be hovering or clicking on its parent elements.
  + **Event Bubbling**: The event starts at the most specific node and flows outwards.  This is default.
  + **Event Capturing**: The event starts at the least specific and flows inward.
+ The flow of elements matters when you have different events on an element and its ancestors.
+ In the event handler the final boolean controls the flow.
  + `true` = capturing phase
  + `false` = bubbling phase

#### The Event Object




[Back to the main page](../README.md)