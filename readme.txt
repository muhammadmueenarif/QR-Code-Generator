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