LOL
===
<!DOCTYPE html>
<html>
<!--
  Created using jsbin.com
  Source can be edited via http://jsbin.com/lakox/6/edit
-->
<head>
<script src="http://code.jquery.com/jquery-git2.js"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/raphael/2.1.0/raphael-min.js"></script>
  <meta charset="utf-8">
  <title>JS Bin</title>

<style id="jsbin-css">

</style>
</head>
<body>
<button id="carlos">
  Animate
  </button>
  
<script>
var height = 500;
var width = 500;
var time=1000;
var numberofsquares=10;


var imageURL= "http://media.tumblr.com/tumblr_lnwltqhA7R1qzj7lm.png";

var paper = Raphael(100,100,height,width);
var r = [];
for (var i=0; i<numberofsquares; i++) {
  r[i] =paper.image(imageURL,120,120,150,100);
}

function jazz() {
 var w=[];
 var h=[];
  for (var i=0; i<numberofsquares; i++) {
    w[i]= Math.random()*width;
    h[i]= Math.random()*height;
  } 
  for (var j=0; j<numberofsquares; j++) {
    r[j].animate({x:w[j],y:h[j]}, time);
  }
    
  r[numberofsquares-1].animate({x:w[numberofsquares-1], y:h[numberofsquares-1]}, time,jazz);
}
$("#carlos").click(jazz);
</script>
</body>
</html>
