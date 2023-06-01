## •Team Introduction<br>
202011267 김승찬 (indiviual, team num 8)<br>
## •Topic Introduction<br>
Neural Style Transfer(화풍을 바꾸는 머닝 러싱)<br>
Choice content-image and style image<br>
The content image is then redrawn in the style of the style image
## •Results<br>

### input
<div class="image-container">
  <img src="/output/combined_a01_candy height 50~1200/a01.jpg" width="314" height="440" />
  <img src="/output/combined_a01_candy height 50~1200/candy.jpg" width="314" height="440" />
</div>

### output
<br>
<div class="image-container">
<img src="/output/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
<img src="/output/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_1200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
 </div>


## •Analysis/Visualization <br>
(empty)<br>
## •Installation<br>
#### Reference repository : https://github.com/gordicaleksa/pytorch-neural-style-transfer<br>
You need to install anaconda, pytorch, python<br>
Install to python (pip install <b> numpy, pip, matplotlib, torchvision, pytorch, opencv-python</b>)<br>
Git clone this repository<br>

###process enviroment
os:window 11 64 bit
processer: AMD Ryzen 5 5600H with Radeon Graphics


아나콘다 설치법

파이토치 설치법

### Setup
  1. Open Anaconda Prompt and navigate into project directory `cd path_to_repo`
  2. Run `conda env create` (while in project directory)
  3. Run `activate pytorch-nst`
### Usage
  1. Copy content images to the default content image directory: `/data/content-images/`
  2. Copy style images to the default style image directory: `/data/style-images/`
  3. Run to cmd or Anaconda Prompt `python neural_style_transfer.py --content_img_name <content-img-name> --style_img_name <style-img-name>`<br>
  ex) `python neural_style_transfer.py --content_img_name lion.jpg --style_img_name candy.jpg`
## •Presentation<br>
(empty)<br>
