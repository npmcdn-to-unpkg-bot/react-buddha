# react-buddha

## A simple React.js page with 4 states

This simple page was written in React.js, with plain Javascript.  I thoroughly examined the React script types(JSX, Harmony, etc), and while I found them readable and understandable, they had more "syntactic sugar" than I'm used to.  Since they didn't seem to add any needed functionality, perhaps these would apppeal to newer coders(the boot-camp crowd).  I already know Javascript extensively, so I decided to use that.

## The four states

### State one: prime

The first state is a blank white page with an error message.  If the script fails, the page will never get past this state, and the user will have to examine the console to see what went wrong.  If the script runs successfully, this state should only be shown for a second.

### State two through four

The rest of the states will appear to cycle between each other.  The timing of the scripts plays in accordance with the remainder gotten when the "elapsed time" is divided by ten.  At second 1, the script will appear to begin, then it will change at seconds 4 and 7, according to the following code, embedded directly into the html for easy reference:

```js    
buddhaDiv = document.getElementById("buddha");
if (seconds % 10 == 1){
  document.body.style.backgroundImage = "url('nature1.jpg')";
  buddhaDiv.innerHTML = "<h2>Master your words</h2>";
  buddhaDiv.style.color = "#33FF22";
}
if (seconds % 10 == 4){
  document.body.style.backgroundImage = "url('nature2.jpg')";
  buddhaDiv.innerHTML = "<h2>Master your thoughts</h2>";
  buddhaDiv.style.color = "white";
}
if (seconds % 10 == 7){
  document.body.style.backgroundImage = "url('nature3.jpg')";
  buddhaDiv.innerHTML = "<h2>Never allow your body to do harm</h2>";
  buddhaDiv.style.color = "yellow";
}
```

The DOM elements are directly accessed via the buddhaDiv object, which is linked to the page element with the ID of "buddha".  This is a div that is empty upon initial execution, and gets filled with a short excerpt from the Dhammapada.  Upon page transition, the background image is also changed via the DOM.


