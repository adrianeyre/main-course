# JQuery

## Download
JQuery can be downloaded from [http://jquery.com/download/](http://jquery.com/download/)

## Running JQuery when the form is ready
```
$(document).ready(function(){
  // Code
})
```

## Object selection
```
$("p") // selects all the paragraph elements
$("#foo") // selects the element with the id foo
$(".bar") // selects all the elements in the bar class
$("[src]") // selects all the elements with a src attribute
$("tr:even") // selects all the even
```

## HTML interaction
`$('#idName').text("New Text")` = change text for the id `idName`<br>

`$("#idDropDownList").val("value")` = change value of the dropdown list `idDropDownList`<br>

`$('#idName').attr('class', "New Class")` = change the CSS for `idName` to `New Class`<br>

`$('#idName').css('border', '1px solid #e8e8e8')` = assign CSS for `idName`<br>

`$("#idName").hide()` = hide `idName`<br>

`$("#idName").show()` = show `idName`<br>

`$("p").addClass("#idName")` = adds the class to `idName`<br>

## Check for events

* Click events
```
$("#buttonId").click(function(){
  // Code
});
```
* Get Statment
```
$.get('http://api' , function(data){
  // Code
});
 ```
* Get JSON Statment
```
$.getJSON("http://api", function(result){
  // Code
});
```
* Post Statment
```
$.post("http://api",{"city":city, "key":value})
```
