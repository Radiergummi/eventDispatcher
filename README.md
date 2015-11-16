# eventDispatcher
A simple way to dispatch and listen to custom events in JS

## Usage

Usually you want some property of your objects to be an `eventDispatcher`, so you can refer to it. This may look like so:  
````javascript
var eventDispatcher = new EventDispatcher()
````
<br>
Now, you can assign event handlers:  
````javascript
eventDispatcher.on('myOwnEventName', function(eventName, data) {
    console.log(eventName + ' has just been triggered. Additional data: ' + data.message)
})
````
<br>
And trigger them:  
````javascript
function myFunction() {
  // do something
  this.eventDispatcher.trigger('myOwnEventName', { message: 'foo' })
}
````
