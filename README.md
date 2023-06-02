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
  <img src="example_image/combined_a01_candy height 50~1200/a01.jpg" width="314" height="440" />
  <img src="example_image/combined_a01_candy height 50~1200/candy.jpg" width="314" height="440" />
</div>

### output
<br>
<div class="image-container">
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_1200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" /> 
 </div>


## •Analysis/Visualization <br>

우선 본문에서 다룰 해당 머닝 러신에서의 변수는 총 4가지 있습니다.<br>
1. tv weight (total variation loss weight) 
2. height
3. content weight
4. style weight

먼저 tv weight을 설명 드리겠습니다. total variation loss weight를 간단히 설명 드리자면 "원본 이미지가 유지되는 영향의 정도"입니다.
tv weight의 수치가 높을 수록 원본이미지에 가까운 이미지가 나옵니다.
아래 이미지는 원본 이미지와 tv weight의 수치를 높인 이미지들 입니다.

<img src="example_image/combined_m1_mosaic1/m1.jpg" height="200" /><br>
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="200" />
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_100.0.jpg" height="200" />
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_10000.0.jpg" height="200" />
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1000000.0.jpg" height="200" />
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_100000000.0.jpg" height="200" />
<img src="example_image/combined_m1_mosaic1/m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_10000000000.0.jpg" height="200" /><br>

위 이미지들은 차례로 오른쪽으로 갈때마다 tv weight의 수치를 100배씩 증가 시켰습니다.<br>

다음 살펴볼 이미지는 height수치입니다. height는 화질입니다. 

<img src="example_image/combined_a01_candy height 50~1200/a01.jpg" height="300" /><br>
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_50_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_100_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_800_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image/combined_a01_candy height 50~1200/a01_candy_o_lbfgs_i_content_h_1200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" /><br>

다음 살펴볼 이미지는 content weight수치입니다.<br> 
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2.jpg" height="300" /><br>
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1.e0.0_sw_30000.0_tv_1.0.jpg" height="300">
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1e2.0_sw_30000.0_tv_1.0.jpg" height="300">
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1e4.0_sw_30000.0_tv_1.0.jpg" height="300">
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1e6.0_sw_30000.0_tv_1.0.jpg" height="300">
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1e8.0_sw_30000.0_tv_1.0.jpg" height="300">
<img src="example_image/combined_c2_wave_crop tv weight 0~12/c2_wave_crop_o_lbfgs_i_content_h_1200_m_vgg19_cw_1e12.0_sw_30000.0_tv_1.0.jpg" height="300">

다음 살펴볼 이미지는 style weight수치입니다.<br> 
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1.jpg" height="250" /><br>
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e0._tv_1.0.jpg" height="250">
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e2.0_tv_1.0.jpg" height="250">
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e4.0_tv_1.0.jpg" height="250">
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e6.0_tv_1.0.jpg" height="250">
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e8.0_tv_1.0.jpg" height="250">
<img src="example_image/combined_b1_okeffe_red_canna style weight 0~10/b1_okeffe_red_canna_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3e10.0_tv_1.0.jpg" height="250"><br>

다음은 제가 애용하는 배경하면에 여러 바이레이션을 넣은 사진입니다.<br>
<img src="example_image/v1/sum.jpg" height="1000" /><br>

## •Installation<br>

### test enviroment<br>
os: window 11 64 bit<br>
processer: AMD Ryzen 5 5600H with Radeon Graphics<br>

anaconda, pytorch, python이 필요합니다.<br>
python에 다음과 같은 것들이 install되어 있어야합니다. (pip install <b> numpy, pip, matplotlib, torchvision, pytorch, opencv-python</b>) <br>
자세한 것은 environment.yml을 참조하세요<br>
이 repository이 clone되어 있어야 합니다.<br>

### anaconda 설치법
다음 공식 홈페이지에서 다운 받을수 있습니다 (https://www.anaconda.com/download/)<br>
1.다운받은 파일을 실행합니다.<br>
2.동의 후 사용자를 선택해줍니다.<br>
3. 설치 경로를 지정해줍니다. 이 때 3.0GB 용량이 필요합니다.<br>
4. 설치가 시작고 끝난 후 finish를 눌러줍니다.<br>

### pytorch 설치법
1. 다음 홈페이지에서 자신에게 맞는 환경을 선택합니다.(https://pytorch.org/get-started/locally/)<br>
2. 저의 환경에서는 아래의 옵션을 선택했습니다..<br> <img src="example_image/pytorch.png"/><br>
당신은 당신에게 맞는 환경을 선택하신 후 홈페이지에서 가르켜준 코드를 실행하면 됩니다.<br>
  

### Setup
  1. Anaconda Prompt를 실행하고 프로젝트 파일의 위치로 이동합니다. `cd path_to_repo`<br>
  2. `conda env create`를 실행합니다. (파일의 위치에 있는 동안)<br>
  3. `activate pytorch-nst`를 실행합니다.<br>
### Usage
  1. `/data/content-images/`에 바꾸고자 하는 그림의 content image 이미지를 저장시킵니다.<br>
  2. `/data/style-images/`에 선택하고 싶은 그림체의 style images 이미지를 저장시킵니다.<br>
  3. 명령 프롬포트 또는 Anaconda Prompt를 실행 후 프로젝트 파일로 이동 후  `python neural_style_transfer.py --content_img_name <content-img파일 이름> --style_img_name <style-img파일 이름>` 을 실행합니다.<br>
  ex) a01.jpg, v5.png 선택 시: `python neural_style_transfer.py --content_img_name a01.jpg --style_img_name v5.png` <br>
  위 ex)코드를 성공적으로 실행시켰고 기다리면 아래 이미지와 유사한 이미지가 `/data/output-images`에 저장될것입니다.<br>
  <img src="example_image/a01_v5_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" width="314" height="440" />
  <br>
  이제 여러 그림을 선택하고 실행하여 만들고 싶은 이미지를 만드시면 됩니다.<br>
  
## •Presentation
(empty)<br>
