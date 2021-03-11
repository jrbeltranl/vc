# Image and video processing
Taking an image and applying a "negative" filter

> :P5 width=720, height=560
> 
> function setup() {
>   PImage photo1;
>   createCanvas(720, 560);
>   noLoop();
>   noStroke();
> }
>
> function draw() {
>   background(0,0,0);
>   int halfImage = width*height/2;
>   photo1 = loadImage("landscape.jpg");
>   photo1.resize(300,500);
>   image(photo1, 0, 0);
>   loadPixels();
>   for (int i = 0; i < halfImage; i++) {
>       float r = 255-red(pixels[i]);
>       float g = 255-green(pixels[i]);
>       float b = 255-blue(pixels[i]);
>       color c = color(r,g,b);
>       pixels[i+halfImage] = c;
>   }
>   updatePixels();
> }

Here is the code for the above:

```md
> PImage photo1;
> void setup() {
>   size(1000, 1000);
> }

> void draw() {
>  background(0,0,0);
>  int halfImage = width*height/2;
>  photo1 = loadImage("landscape.jpg");
>  photo1.resize(1000,500);
>  image(photo1, 0, 0);
>  loadPixels();
>  for (int i = 0; i < halfImage; i++) {
>      float r = 255-red(pixels[i]);
>      float g = 255-green(pixels[i]);
>      float b = 255-blue(pixels[i]);
>      color c = color(r,g,b);
>      pixels[i+halfImage] = c;
> }
>  updatePixels();
>}

```

> :ToCPrevNext
