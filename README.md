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

### test enviroment<br>
os:window 11 64 bit<br>
processer: AMD Ryzen 5 5600H with Radeon Graphics<br>

### anaconda 설치법
다음 공식 홈페이지에서 다운 받을수 있습니다 (https://www.anaconda.com/download/)<br>
1.다운받은 파일을 실행합니다.
2.동의 후 사용자를 선택해줍니다.
3. 설치 경로를 지정해줍니다. 이 때 3.0GB 용량이 필요합니다.
4. 설치가 시작고 끝난 후 finish를 눌러줍니다.

### pytorch 설치법
1. 다음 홈페이지에서 자신에게 맞는 환경을 선택합니다.(https://pytorch.org/get-started/locally/)
2. 제 환경에서는 아래의 옵션을 선택했습니다..<br> <img src="/output/pytorch.png"/><br>
당신에게 맞는 환경을 선택하신 후 실행시키면 됩니다.<br>
다음 홈페이지에서 가르켜준 코드를 실행하면 됩니다.<br>
  

### Setup
  1. Anaconda Prompt를 실행하고 프로젝트 파일의 위치로 이동합니다. `cd path_to_repo`
  2. `conda env create`를 실행합니다. (파일의 위치에 있는 동안)
  3. `activate pytorch-nst`를 실행합니다.
### Usage
  1. `/data/content-images/`에 바꾸고자 하는 그림의 content image이미지를 저장시킵니다.
  2. `/data/style-images/`에 선택하고 싶은 그림체의 style images이미지를 저장시킵니다.
  3. 명렬프롬포트 또는 Anaconda Prompt를 실행 후 프로젝트 파일로 이동 후  `python neural_style_transfer.py --content_img_name <content-img파일 이름> --style_img_name <style-img파일 이름>` 을 실행합니다.<br>
  ex) `python neural_style_transfer.py --content_img_name a01.jpg --style_img_name v5.png`
## •Presentation<br>
(empty)<br>
