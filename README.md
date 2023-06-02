## •Team Introduction<br>
202011267 김승찬 (indiviual, team num 8)<br>
## •Topic Introduction<br>
Neural Style Transfer(화풍을 바꾸는 머닝 러싱)<br>
그림체를 바꾸고 싶은 그림과 바꿀 그림체를 선택하고 실행시킵니다.<br>
그러면 당신이 고른 그림체를 학습하여 화풍이 바뀐 새로운 그림이 나올겁니다.<br>
#### 참조 repository :  https://github.com/gordicaleksa/pytorch-neural-style-transfer<br>
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
1. height
2. content weight
3. style weight
4. tv weight (total variation loss weight) 

각 수치의 기본 값들은 height =400, content weight=1e5, style weight=3e4, tv weight=1e0 입니다.<br>
별도로 명시하지 값들을 제외한 값들은 기본 값들을 가지고 있습니다.

#### height
우선 살펴볼 이미지는 height수치입니다. height는 간단히 말하자면 화질입니다. 

<img src="example_image\combined_d1_v4 height/d1.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/v4.png" height="300" /><br>
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_50_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_100_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_800_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<img src="example_image\combined_d1_v4 height/d1_v4_o_lbfgs_i_content_h_1200_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="300" />
<br>
위 이미지 들은 원본 이미지와 각 height 수치에만 변동을 준 이미지들 입니다. (왼쪽 위 부터height = 50, 100, 200, 400, 800, 1200)<br>
height수치가 높아질수록 확인되는 점들을 말씀 드리겠습니다.<br>
<br>
1. 해상도가 올라간다. 사진을 확대하여 픽셀을 확인한다면 height의 수치가 높을수록 사진을 이루는 픽셀의 크기가 작아진다는 점이 확인됩니다.
2. 원본 이미지와의 유사도가 높아진다. height 수치가 낮은 50~200에서의 사진은 뒤쪽의 집은 커녕 말도 확인이 힘든 반면 400부터는 말과 집의 현상이 육안으로 쉽게 구분됩니다. 그 외에도 해상도가 높아질수록 낮은 height수치에서는 발견되지 않은 원본 이미지의 세세한 부분이 확인되었습니다.<br>

 추가로 height수치가 올라갈수록 프로그램의 실행 시간이 증가하였습니다.

#### content weight

다음 살펴볼 이미지는 content weight수치입니다.<br> 
content weight는 원본 이미지의 색상을 얼마나 유지할지를 정하는 변수입니다.<br>
<img src="example_image\combined_h1_vg_self content\h1.jpg" height="270" />
<img src="example_image\combined_h1_vg_self content\vg_self.jpg" height="270" /><br>
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_1.0_sw_30000.0_tv_1.0.jpg" height="270">
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_100.0_sw_30000.0_tv_1.0.jpg" height="270">
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_10000.0_sw_30000.0_tv_1.0.jpg" height="270">
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_1000000.0_sw_30000.0_tv_1.0.jpg" height="270">
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_100000000.0_sw_30000.0_tv_1.0.jpg" height="270">
<img src="example_image\combined_h1_vg_self content\h1_vg_self_o_lbfgs_i_content_h_400_m_vgg19_cw_10000000000.0_sw_30000.0_tv_1.0.jpg" height="270">
위 이미지 들은 원본 이미지와 각 content weight 수치에만 변동을 준 이미지들 입니다. ( 왼쪽 위 부터 content weight = 1e0, 1e2, 1e4, 1e6, 1e8, 1e10)<br>
육안상으로는 (1e0 ~1e4)에서는 각 이미지의 차이를 확인하기 어렵습니다. 1e6에서 약간의 차이가 보이며, 1e8부터는 육안상 차이를 쉽게 확인 할 수 있으며 1e10은 원본과 유사한 색상을 가지고 있습니다.<br>
(1e0 ~1e4)에서 차이가 확인되지 않은 이유는 비록 1e2씩 커져서 1e4까지 커지지만 수치가 style weight의 기본 값인 3e4와 수치를 비교하면 큰 차이가 나지 않아서 그런 것 같습니다. 그래서 style weight의 기본값을 넘어서는 1e6부터 차이가 롹인되는것 같습니다.<br>

#### style weight

다음 살펴볼 이미지는 style weight수치입니다.<br>
style weight는 style img의 화풍 output에 영향을 얼마나 끼칠지를 정하는 변수입니다.<br>
<img src="example_image\combined_s1_a02 style\s1.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\a02.jpg" height="350" /><br>
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3.0_tv_1.0.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_300.0_tv_1.0.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_3000000.0_tv_1.0.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_300000000.0_tv_1.0.jpg" height="350" />
<img src="example_image\combined_s1_a02 style\s1_a02_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000000000.0_tv_1.0.jpg" height="350" /><br>
위 이미지 들은 원본 이미지와 각 style weight 수치에만 변동을 준 이미지들 입니다. ( 왼쪽 위 부터 style weight = 3e0, 3e2, 3e4, 3e6, 3e8, 3e10)<br>
먼저 처음 사진 부터 원본 이미지와 차이가 보입니다. 하지만 화풍에 영향을 준것이 아닌 색상만 바겼을 뿐 그림체에 영향을 거의 주지 않았습니다.<br>
하지만 3e2부터 그림체가 급격히 바뀌더니 3e4~3e10부터 육안으로는 구분안되는 똑같은 그림체를 가지게 되었습니다.<br>
content weight인 1e5에 근접하는 3e4부터 그 이후의 값들은 유사한 겨로가를 도출하였습니다. 

#### tv weight (total variation loss weight) 

먼저 tv weight을 설명 드리겠습니다. total variation loss weight를 간단히 설명 드리자면 "원본 이미지가 유지되는 영향의 정도"입니다.
tv weight의 수치가 높을 수록 원본이미지에 가까운 이미지가 나옵니다. 추가로 tv weight가 output 그림체의 부드러움(선명도)도 영향을 끼칩니다.<br>
아래 이미지는 원본 이미지와 tv weight의 수치를 높인 이미지들 입니다.

<img src="example_image\combined_m1_mosaic1 tv weight\m1.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\mosaic.jpg" height="200" /><br>
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1.0.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_100.0.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_10000.0.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_1000000.0.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_100000000.0.jpg" height="200" />
<img src="example_image\combined_m1_mosaic1 tv weight\m1_mosaic_o_lbfgs_i_content_h_400_m_vgg19_cw_100000.0_sw_30000.0_tv_10000000000.0.jpg" height="200" /><br>

위 이미지 들은 원본 이미지와 각 tv weight 수치에만 변동을 준 이미지들 입니다. ( 왼쪽 위 부터 tv weight = 1e0, 1e2, 1e4, 1e6, 1e8, 1e10)<br>
tv weight 수치가 높아 질수록 화풍이 끼치는 영향이 낮아지고 있는것이 확인됩니다.<br>
tv weight 수치가 낮은 1e0, 1e2는 style img의 영향이 크게 끼치지만, 1e4, 1e6부터 style img의 영향이 점차 사라지며 원본 이미지의 영향이 커지며, tv weight가 높은 1e8, 1e10은 style img의 영향이 확인되지 않습니다.<br>
추가로 tv weight수치가 높아질수록 output의 그림체의 선명도가 낮아지는 것이 확인됩니다.

#### 정리


다음은 제가 애용하는 배경하면에 여러가지 style img를 넣은 사진입니다.<br>
<img src="example_image/v1/sum.jpg" height="1000" /><br>
가운데 있는 사진이 원본입니다. 만약 여러분들도 이 repository에 관심이 있다면 좋아하는 사진에 여러 style img를 넣어 repository를 실행시켜 보세요.

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
