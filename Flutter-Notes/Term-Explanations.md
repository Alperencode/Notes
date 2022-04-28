# Term Explanations

Explanations of general terms and logic

<br><hr>

## 1) Life Cycle

### a. InitState

First Lifecycle method that is called when the widged is created. This method will be called **before the build** method.

<br>

### b. DidChangeDependencies

Second Lifecycle method that is called directly after 'initstate'. That will be called for **every dependency change**.

<br>

### c. DidUpdateWidget

Called whenever a configuration changes for that specific widget. That could be things like passing variables down the constructer and those variables update. <br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A very common usage case is when you pass a duration for an animation controller as you then need to change the duration of that controller.

<br>

### d. Deactivate

Called when object is removed from the tree. This is not dispose anything. This method can be called for example moving the widget in the widget tree using a GlobalKey.

<br>

### e. Dispose

Called when object is removed from the tree permanently. One example of when its called is when you call the 'Navigator.pushReplacement' and actually replace the current widget with another one.

<hr><br>