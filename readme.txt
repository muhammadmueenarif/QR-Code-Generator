To create a file using cmd, use touch command or use echo "This is readme file"> readme.

Google Chart API will be used to create qr code. the url of api is: https://chart.googleapis.com/chart?

Some parameters we need to add in url. 
cht=qr. This is required. used to specify qr code.
chs=<width>x<height>. it tells image size. it is also required. 
chl=data. it is also required. it is the data that will be encode like digits, alphanumeric, or binary. 

for example, chart.googleapis.com/chart?cht=qr&chs=150x150&chl=Hello.
Copy and paste this in browser. it will show qr code of 150 by 150. 
if we scan that code, it will show the word Hello. 

To use google chart api in js, 
We need to get input from the user in which he will specify the text that will store in qr code. 
They will also specify height and width of qr code. 
We will use text area for qr code text and use drop down list for height and width. 

Now open vs code and create file. use ! and hit enter, it will write default code. 
Next write js script. you can do this by script tag or create a new file qrcode.js. <script src="script.js"></script>.

If we want to perform action, then write function, code for it. 
alert("How are you"); for output. 
getElementById.value, getElementByclassName, are used to access elements of html. 

if we want to access value of an element paragraph, p or div tag, we will change it to document.getElementById.innerHtml 
instead of value.
use select tag to make options and use .value to access which option is selected. 
when to show image, then replace .value, .innerHtml with .src. it will show path of image. 

How to change values of accessed elements?
if using p tag, then write .innerHtml="write changed text that will display";
Same method to change for div tag. 

If we want to change src of img, then write .src="paste image url here";

If we give 4 options, and display img of each option on selection of 3 names, and want to show error message 
if 4 option is selected than use if else. we use select and option. give id to select tag and write a default 
image tag with empty src and id. use this as default in the function of onclick. create variable to access text 
from select option. 

then use if to check which option is selected and change img src to that option based on text.
function Showit() {
  var theimg=document.getElementById("myimg");
  var thetext=document.getElementById("myoption").value;
  
  if(thetext=="Google")
  {
    theimg.src="https://images.unsplash.com/photo-1715604535941-3a38ad63bd79?q=80&w=1471&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D";
  }
  else if(thetext=="Bing") {
     theimg.src="https://images.unsplash.com/photo-1715550722304-b6ee97071817?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D";
  }
  else if (thetext=="Yahoo") {
    theimg.src="https://images.unsplash.com/photo-1715645973101-f07bc6951c03?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
  }
  else {
    alert("No such source found");
  }
}

</script>

<img src="" alt="" id="myimg">

<select id="myoption">
    <option value="Google">google</option>
    <option value="Bing">bing</option>
    <option value="Yahoo">yahoo</option>
    <option value="FB">fb</option>

</select>

<!-- This is input. Onclick function to perform action  -->
<input type="submit" value="Click Me" onclick="Showit()">


--------------------------------
to select an option as default from multiple, write selected in it. <option value="" selected></option>

