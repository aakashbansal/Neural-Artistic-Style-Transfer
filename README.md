# Neural-Artistic-Style-Transfer
This is a Deep Learning project that implements Neural Style Transfer (transferring a given style to an image) from the paper [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576) by Leon A. Gatys, Alexander S. Ecker, Matthias Bethge. The pre-trained VGG-19 Model is used in this project to extract and work on the deep level features of input and style images.

## Description

The project has two Jupyter notebooks :
1. **neural_single_style_transfer.ipynb** : This transfers the style of one image to a given image.

2. **neural_multiple_style_transfer.ipynb** : This transfers the styles of multiple images to a given image. The notebook is currently configured to transfer styles of two images to a given image but can be conveniently modified to transfer more than two styles to a given input image.

## Note

1. The notebooks were run on **GPU-accelerated** run-time of [Google Colab](https://colab.research.google.com/) where each run of about **2000 iterations** used to take nearly **10 minutes**. On a CPU, it could take about **3-4 hours** or more depending on the clock speed. So, it is preferable to run these notebooks on a GPU.

2. The process of Style Transfer requires a lot of **Hyperparameter Tuning**. Each style and input image requires a different set of hyperparameters that may or may not work on a different style-image pair.


**Tip :** Start with APLHA = 10 and BETA = 5000. Check after 500 iterations. If the outcome is 
not desirable, change accordingly. 
If the content of input image is too much distorted, try 
increasing the value of ALPHA. 
If the image is not attaining the desired style, increase BETA
and if the input is loosing its original content a lot, decrease the value of BETA.
If nothing works, change ALPHA-BETA combinations altogether such as ALPHA = 5 and 
BETA = 100 and see whatever works best for the given combination of input and style image.

For **Multi-Style Transfer**, same guidelines apply along with an additional step. 
Instead of just single BETA value in case of Single Style Transfer, now two values need 
to be considered - BETA1 and BETA2. 
BETA1 and BETA2 needs to be modified depending on whether the final image 
should have more style of first style image ( BETA1 > BETA2), more style of second style image
( BETA1 < BETA2) or should have equal styles of both style images ( BETA1 = BETA2 ).


## Examples

Below are some examples of the images on which Neural Style Transfer was applied and the corresponding ALPHA-BETA combinations are also given along with the effect they have on a given input image.

### Content Images

Following are the input images used in the given project :

<img src="images/content images/baby.jpg" height="220" width="285"> <img src="images/content images/baby3.jpg" height="220" width="285">  <img src="images/content images/build.jpg" height="220" width="285"> <img src="images/content images/emma.jpg" height="220" width="285"> <img src="images/content images/minions.jpg" height="220" width="285"> <img src="images/content images/scenery.jpg" height="220" width="285"> <img src="images/content images/dancing girl.jpg" height="350" width="285"> <img src="images/content images/night king.jpg" height="350" width="285"> 

### Style Images

Following are the style images used in the given project :

<img src="images/style images/burnt_gold.jpg" height="220" width="285"> <img src="images/style images/random colors.jpg" height="220" width="285"> <img src="images/style images/red-canna.jpg" height="220" width="285"> <img src="images/style images/vector-landscape.jpg" height="220" width="285"> <img src="images/style images/style2.jpg" height="220" width="285"> <img src="images/style images/style3.jpg" height="220" width="285"> <img src="images/style images/style4.jpg" height="350" width="285">  <img src="images/style images/seated-nude.jpg" height="350" width="285">

### Output Images
 
 Following are the images styled using Neural Style Transfer technique :
 
 ### Single Style Transfer
 
**ALPHA - 10 and BETA - 100** <br>
 <img src="images/content images/scenery.jpg" height="220" width="250"> + <img src="images/style images/burnt_gold.jpg" height="220" width="250"> =   <img src="images/single-style outputs/burnt_gold a 10 b 100.jpg" height="220" width="250">
 <hr>
 
**ALPHA - 10 and BETA - 5000**<br>
 <img src="images/content images/dancing girl.jpg" height="220" width="250"> + <img src="images/style images/seated-nude.jpg" height="220" width="250"> =   <img src="images/single-style outputs/seated-nude_alpha_10_beta_5000.jpg" height="220" width="250">
 <hr>
 
**ALPHA - 10 and BETA - 5000**<br>
 <img src="images/content images/minions.jpg" height="220" width="250"> + <img src="images/style images/style2.jpg" height="220" width="250"> =   <img src="images/single-style outputs/style2_styled.jpg" height="220" width="250">
 <hr>
 
**ALPHA - 10 and BETA - 5000**<br>
 <img src="images/content images/night king.jpg" height="220" width="250"> + <img src="images/style images/random colors.jpg" height="220" width="250"> =   <img src="images/single-style outputs/random colors_alpha_10_beta_5000.jpg" height="220" width="250">
 <hr>
 
**ALPHA - 10 and BETA - 5000**<br>
 <img src="images/content images/baby.jpg" height="220" width="250"> + <img src="images/style images/vector-landscape.jpg" height="220" width="250"> =   <img src="images/single-style outputs/vector-landcape a 10 b 1500.jpg" height="220" width="250">
 <hr>
 
 **ALPHA - 10 and BETA - 20**<br>
 <img src="images/content images/build.jpg" height="220" width="250"> + <img src="images/style images/style2.jpg" height="220" width="250"> = <img src="images/single-style outputs/style2_alpha_10_beta_20.jpg" height="220" width="250">  
 <hr>
 
 **ALPHA - 10 and BETA - 250**<br>
 <img src="images/content images/baby3.jpg" height="220" width="250"> + <img src="images/style images/vector-landscape.jpg" height="220" width="250"> = <img src="images/single-style outputs/vector-landcape a 10 b 250.jpg" height="220" width="250"> 
<hr>

**ALPHA - 10 and BETA - 500**<br>
 <img src="images/content images/emma.jpg" height="220" width="250"> + <img src="images/style images/red-canna.jpg" height="220" width="250"> = <img src="images/single-style outputs/red-canna a 10 b 500.jpg" height="220" width="250">    
<hr>

**ALPHA - 10 and BETA - 6000**<br>
 <img src="images/content images/emma.jpg" height="220" width="250"> + <img src="images/style images/style3.jpg" height="220" width="250"> = <img src="images/single-style outputs/style3 a 10 b 6000.jpg" height="220" width="250"> 
 <hr>
 
 <img src="images/content images/emma.jpg" height="220" width="250"> + <img src="images/style images/style4.jpg" height="220" width="250"> =
<img src="images/single-style outputs/style4 a 10 b 3000.jpg" height="260" width="400"> **ALPHA - 10 and BETA - 3000**<br> 
<img src="images/single-style outputs/style4  a 10 b 2500.jpg" height="260" width="400"> **ALPHA - 10 and BETA - 2500**<br> 
<img src="images/single-style outputs/style4 a 10 b 1000.jpg" height="260" width="400"> **ALPHA - 10 and BETA - 1000**<br> 

As can be seen in these images, when we decrease the value of BETA, the overpowering effect of Style image is being reduced and generated image is looking more pleasant.<br> 
<hr>

 ### Multiple Style Transfer
 
 <img src="images/content images/emma.jpg" height="220" width="250"> + <img src="images/style images/burnt_gold.jpg" height="220" width="250"> + <img src="images/style images/random colors.jpg" height="220" width="250"> = <br>
<img src="images/multi-style outputs/burnt_gold and random colors a 10 b1 1500 b2 1500.jpg" height="260" width="400">
**ALPHA - 10 BETA1 - 1500 BETA2 - 1500**<br> 
<img src="images/multi-style outputs/burnt_gold and random colors a 10 b1 2200 b2 800.jpg" height="260" width="400">
**ALPHA - 10 BETA1 - 2200 BETA2 - 800**<br> 

As is apparent from above two images when BETA1 is increased and BETA2 is decreased for the second image, style of first image increases considerably while the style of second image somewhat fades in.
<hr>

**ALPHA - 10 BETA1 - 1500 BETA2 - 15000**<br>
 <img src="images/content images/dancing girl.jpg" height="220" width="250"> + <img src="images/style images/red-canna.jpg" height="220" width="250"> + <img src="images/style images/seated-nude.jpg" height="220" width="250"> = <br>
 <img src="images/multi-style outputs/red -canna and seated-nude a10 b1 1500 b2 1500.jpg" height="400" width="300"> 
 <hr>
 
 **ALPHA - 10 BETA1 - 50 BETA2 - 100**<br>
 <img src="images/content images/build.jpg" height="220" width="250"> + <img src="images/style images/style2.jpg" height="220" width="250"> + <img src="images/style images/style4.jpg" height="220" width="250"> = <br>
 <img src="images/multi-style outputs/style2 and style 4 a 10 b1 50 b2 100.jpg" height="260" width="400"> 
 <hr>
 
 <img src="images/content images/baby.jpg" height="220" width="250"> + <img src="images/style images/seated-nude.jpg" height="220" width="250"> + <img src="images/style images/vector-landscape.jpg" height="220" width="250"> = <br>
<img src="images/multi-style outputs/seated nude and vector landscape a 10 b1 2500 b2 1750.jpg" height="260" width="400">
**ALPHA - 10 BETA1 - 2500 BETA2 - 1750**<br> 
<img src="images/multi-style outputs/seated nude and vector landscape a 10 b1 3500 b2 1750.jpg" height="260" width="400">
**ALPHA - 10 BETA1 - 3500 BETA2 - 1750**<br> 
<img src="images/multi-style outputs/seated nude and vector landscape a 10 b1 5000 b2 1500.jpg" height="260" width="400">
**ALPHA - 10 BETA1 - 5000 BETA2 - 1500**<br> 

As can be seen in these images, when we increase the value of BETA1, the effect of First Style image increases on the final input image while the effect of second style image decreases.<br> 
<hr>

 
