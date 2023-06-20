# Neural_Feature_Exchange
**Generates artistic images by transferring the style of one image onto another to give a composite &amp; stylized image.**

Deployed Model : 
## What is Neural Style Transfer ?
_In simple words it is an algorithm where we combine the style of one input image I_s with the content of another input image I_c to generate a new image
I_o with the style of the first and content of the second image._

Content includes- Objects, shapes and the overall structure and geometry of given image.<br>
Style includes- Textures, colors, and the patterns.

## Lets take it Step by Step...
<ol>
<li> Choose a Content Image I_c and a Style Image Is to generate a final image I_o. </li>
<li> Loading a pre-trained convolutional neural network, in this case VGG-19</li><br>
  


 <br>
<li> The next step is to define the loss functions that will guide the training pipeline into generating our desired image I_o. <br> We do this using two loss functions: <br>
<ul>
  <li> The <b>Content loss function</b> measures the difference between the features of the generated image I_o and the features of the content image I_c</li>
  <li> The <b>Style loss function</b> measures the difference between the features of the generated image I_o and the features of the style image I_s. </li>
  <li>We get a total loss function by combining these two loss functions and taking their weighted sum as :</li><br>
  
  
</ul>
</li>
<li>The generated Image I_o is first initialized with the same pixels as the content image I_c. <br> During training, it is gradually optimized to the match the style of I_s, retaining only the content of I_c</li>
<li>The whole process is repeated for many epochs until we end up with desired output I_o.</li>
</ol>







## References:-
<ul>
  <li>https://arxiv.org/pdf/1508.06576.pdf</li>
  <li>https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf</li>
</ul>
 




