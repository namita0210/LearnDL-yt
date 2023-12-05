<h2>COMPUTER VISION</h2>
<p>When we talk of computer vision we are dealing with two types of data - pictures and videos. When an image is stored it is broken down into components called pixels. 
Pixels are said to be the smallest unit of an image, they represent only one colour. For each picel to represent a certain colour we have a pixel intensity.
If the dimension of an image is 50X50 then to represent the intensity of each pixel in that image we can do that with a 2D matrix of dimension 50X50, each element of that matrix
will represent the picture intensity in a numeric value - where the min and max value each pixel can have will be 0 or 255.
In grayscale : 0 = black  and 255 = white.</p>

<h2>HOW IS A COLOUR IMAGE REPRESENTED</h2>
<p>Each color image is made up of 3 color channels - RGB
Mathematically they can be represented as a multidimensional array.
If the dimensions of an image is 50X50 and it is a colored image then it will be represented as 50,50,3 -> 50X50 representing the image size and 3 representing the number of channels.</p>

<h2>HOW IS A VIDEO REPRESENTED</h2>
<p>It is a collection of images</p>

<h2>INTUITION BEHIND CONVOLUTION</h2>
<p>We place our filter on top of image and move it horizontally from left to right  and top to bottom one pixel at time.
We have to multiply the kernel/filter matrix values with the input image pixel values and then add them together to get the transformed output</p>

<h2>PADDING</h2>
<ul>When we use a 3X3 kernel on a 5X5 image the transformed image in the output is of the size 3X3. Why?</ul>
<ul>This happens because the kernel can not be placed on the corner pixel values of the input image and thus it loses dimensions on all edge cases</ul>
<ul>To not lose dimension along each axiss - we use padding.</ul>
<ul>In padding we add a new dimension of blank values before we perform convolution</ul>
<ul>Padding is pixel values that are equal to 0.</ul>

<button>Till now we have understood how convolution works on a grayscale image, let us find out how it will work on a coloured image.</button>
<ul> In color images - we apply a filter on each of the channels and then perform aggregation of the resul to get final transformed color image.</ul>