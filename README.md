## •Team Introduction<br>
202011267 김승찬 (indiviual, team num 8)<br>
## •Topic Introduction<br>
Neural Style Transfer(화풍을 바꾸는 머닝 러싱)<br>
https://github.com/gordicaleksa/pytorch-neural-style-transfer
## •Results<br>

<div style="display: flex; width: 500px; height: 300px;">
  input<br>
  <img src="/output/combined_a01_candy height 50~1200/a01.jpg" width="314" height="440" />
  <img src="/output/combined_a01_candy height 50~1200/candy.jpg" width="314" height="440" />
  <br>
  output<br>
  <img src="/output/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_1200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
</div>

## •Analysis/Visualization <br>
(empty)<br>
## •Installation<br>
Install anaconda, pytorch(you need cuda)<br>
Install to python (pip install <b>argparse, numpy, matplotlib, torch, pytorch</b>)<br>
### Setup
  1. Open Anaconda Prompt and navigate into project directory `cd path_to_repo`
  2. Run `conda env create` (while in project directory)
  3. Run `activate pytorch-nst`
### Usage
  1. Copy content images to the default content image directory: `/data/content-images/`
  2. Copy style images to the default style image directory: `/data/style-images/`
  3. Run to cmd or Anaconda Prompt `python neural_style_transfer.py --content_img_name <content-img-name> --style_img_name <style-img-name>`
## •Presentation<br>
(empty)<br>
