# jumping_game

Using the following tutorial on [youtube](https://www.youtube.com/watch?v=bG2BmmYr9NQ).

## Key Learning

### Creating an animation using keyframes 

    @keyframes jump {
        0% { top: 180px; }
        35% { top: 100px; }
        65% { top: 100px; }
        100% { top: 180px; }
    }

* Jump is the name of the animation
* % is the percentage through the movement (0 being the start and 100 being the end)
* To use the annimation you would use
        
        animation: jump 500ms;
    
* The time in ms (milliseconds) or s (seconds) is how long the animation will take.
* Animation can be saved as a class which can then be given to an element using js.
* You can use the following:     
    * infinite - allows the animation to continue running 
    * linear - makes the movement even across the screen 

## Keydown

    document.addEventListener('keydown', (event) => {
        if ( event.which == 32 ) {
            jump()
        }
    })

* The keydown event listener will listen to which key is pressed.
* event.which will give a number for the key (32 for the space bar)
* event.code will give a name (for the space bar it would be space)
* For more on on the keyboard codes use this [link](https://css-tricks.com/snippets/javascript/javascript-keycodes/).

## setTimeout() vs setInterval()

### setTimeout()

* Set Timeout will take an expression and a time and will execute the expression after the time given.

        setTimeout(() => alert('Hello'), 1000)

* The alert will fire after 1000ms (1 second).

### setInterval()

* Set Interval will take an expression and a time but will execute the expression repeatedly after the alotted time has passed.

        setInterval(() => alert('Hello'), 3000)

* The alert will fire again and again with a gap of 3000ms (3 seconds)


## window.getComputedStyle()

        const characterTop = parseInt(window.getComputedStyle(character).getPropertyValue('top'))

* window.getComputedStyle(character).getPropertyValue('top') will return a px value, by using the parseInt() we will only get returned the integer.
* The property value for this example will be the css top position value.