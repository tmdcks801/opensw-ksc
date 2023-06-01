## •Team Introduction<br>
202011267 김승찬 (indiviual, team num 8)<br>
## •Topic Introduction<br>
Neural Style Transfer(화풍을 바꾸는 머닝 러싱)<br>
그림체를 바꾸고 싶은 그림과 바꿀 그림체를 선택하고 실행시킵니다.<br>
그러면 당신이 고른 그림체를 학습하여 화풍이 바뀐 새로운 그림이 나올겁니다.<br>
#### 참조 repository : https://github.com/gordicaleksa/pytorch-neural-style-transfer<br>
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

anaconda, pytorch, python이 필요합니다.<br>
python에 다음과 같은 것들이 install되어 있어야합니다. (pip install <b> numpy, pip, matplotlib, torchvision, pytorch, opencv-python</b>) <br>
자세한 것은 environment.yml을 참조하세요<br>
이 repository이 clone되어 있어야 합니다.(https://github.com/tmdcks801/opensw-ksc)<br>

### test enviroment<br>
os: window 11 64 bit<br>
processer: AMD Ryzen 5 5600H with Radeon Graphics<br>

### anaconda 설치법
다음 공식 홈페이지에서 다운 받을수 있습니다 (https://www.anaconda.com/download/)<br>
1.다운받은 파일을 실행합니다.<br>
2.동의 후 사용자를 선택해줍니다.<br>
3. 설치 경로를 지정해줍니다. 이 때 3.0GB 용량이 필요합니다.<br>
4. 설치가 시작고 끝난 후 finish를 눌러줍니다.<br>

### pytorch 설치법
1. 다음 홈페이지에서 자신에게 맞는 환경을 선택합니다.(https://pytorch.org/get-started/locally/)<br>
2. 저의 환경에서는 아래의 옵션을 선택했습니다..<br> <img src="/output/pytorch.png"/><br>
당신은 당신에게 맞는 환경을 선택하신 후 홈페이지에서 가르켜준 코드를 실행하면 됩니다.<br>
  

### Setup
  1. Anaconda Prompt를 실행하고 프로젝트 파일의 위치로 이동합니다. `cd path_to_repo`<br>
  2. `conda env create`를 실행합니다. (파일의 위치에 있는 동안)<br>
  3. `activate pytorch-nst`를 실행합니다.<br>
### Usage
  1. `/data/content-images/`에 바꾸고자 하는 그림의 content image이미지를 저장시킵니다.<br>
  2. `/data/style-images/`에 선택하고 싶은 그림체의 style images이미지를 저장시킵니다.<br>
  3. 명렬프롬포트 또는 Anaconda Prompt를 실행 후 프로젝트 파일로 이동 후  `python neural_style_transfer.py --content_img_name <content-img파일 이름> --style_img_name <style-img파일 이름>` 을 실행합니다.<br>
  ex) `python neural_style_transfer.py --content_img_name a01.jpg --style_img_name v5.png`<br>
  위 ex)코드를 성공적으로 실행시켰고 기다리면 아래 이미지와 유사한 이미지가 `/data/output-images/`에 저장될것입니다..<br>
  <img src="/output/a01_v5_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
  <br>
  
## •Presentation
(empty)<br>
