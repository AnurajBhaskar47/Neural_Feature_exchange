# Neural_Feature_Exchange
**Generates artistic images by transferring the style of one image onto another to give a composite &amp; stylized image.**

## [Deployed Model](https://huggingface.co/spaces/AnJ47/Neural_Feature_exchange)

## What is Neural Style Transfer ?
_In simple words it is an algorithm where we combine the style of one input image I_s with the content of another input image I_c to generate a new image
I_o with the style of the first and content of the second image._

Content includes- Objects, shapes and the overall structure and geometry of given image.<br>
Style includes- Textures, colors, and the patterns.

## Lets take it Step by Step...
<ol>
<li> Choose a Content Image I_c and a Style Image Is to generate a final image I_o. </li>
<li> Loading a pre-trained convolutional neural network, in this case VGG-19</li><br>
  
  ![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/8abb160c-d543-4cb4-ae38-84348102b31e)
  ![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/adf0ea6b-805a-4d63-923a-3d61aed8b2dc)


 <br>
<li> The next step is to define the loss functions that will guide the training pipeline into generating our desired image I_o. <br> We do this using two loss functions: <br>
<ul>
  <li> The <b>Content loss function</b> measures the difference between the features of the generated image I_o and the features of the content image I_c</li>
  <li> The <b>Style loss function</b> measures the difference between the features of the generated image I_o and the features of the style image I_s. </li>
  <li>We get a total loss function by combining these two loss functions and taking their weighted sum as :</li><br>
  
![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/623eb26d-6ee7-4898-abb4-8f80c619bf5a)
	
</ul>
</li>
<li>The generated Image I_o is first initialized with the same pixels as the content image I_c. <br> During training, it is gradually optimized to the match the style of I_s, retaining only the content of I_c</li>
<li>The whole process is repeated for many epochs until we end up with desired output I_o.</li>
</ol>

 ![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/9c93b7fd-a403-4a83-8b0d-cc1bd3b1e15a) ![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/3c6c5ecd-1c26-42ca-b6ac-e5623518e471)
 
 ![image](https://github.com/AnurajBhaskar47/Neural_Feature_exchange/assets/97795939/4ea612d6-c8e4-4f23-a000-ea9cbc5a1e49)





## References:-
<ul>
  <li>https://arxiv.org/pdf/1508.06576.pdf</li>
  <li>https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf</li>
</ul>
 




