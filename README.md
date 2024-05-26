![Screenshot 2023-12-29 at 15 51 15](https://github.com/pass98/DDal_KKak----/assets/123361606/868f5e40-1f7b-4064-acc2-6a8939f7e1ff){: width="300" height="300")


## DDAL_KKAK
## 광주인공지능사관학교4기 JS 특화과정 실전역량프로젝트
### Caffeine is water of life Team


<br/>

### 📌 팀 카페인은 생명수 프로젝트 규칙

#### 1. commit 양식 참고해서 commit하기<br/>
ex) git commit -m '20231109 Login,Join 박지훈'<br/>
#### 2. commit 했으면 프로젝트 단톡에 해당 내용 공유하기<br/>
ex) 20231109 Login,Join 푸쉬 했습니다.<br/>
#### 3. 프론트 - 백 같은 파트 협업해서 개발 시 수정 내용 구두 상으로 공유하기 (충돌방지)


<br/>

### ✏️ 프로젝트 소개
생성형 AI 모델(카카오의 Karlo API, Stable Diffusion 등)을 사용하여 사용자가 입력한 프롬프트를 바탕으로 이미지를 생성,  <br/>
생성된 이미지를 filerobot-image-editor를 이용하여 사용자가 쉽게 이미지를 편집할 수 있는 서비스를 제공합니다.<br/>
생성 및 편집된 이미지를 로고나 포스터에서 활용할 수 있도록 다운로드 기능을 제공하고, 추가로 티셔츠나 머그컵과 같은<br/>
굿즈 제작에 활용할 수 있도록 서비스를 개발 하였습니다.

<br/>

### 🗓️ 프로젝트 기간(기획 ~ 발표)
* 23.10.24 ~ 23.12.5 (43일)

<br/>

### 🫵 팀원 및 역할
* 팀장 : 김지원(PM)
* 팀원 : 김형균(FE)
* 팀원 : 나범수(FE)
* 팀원 : 박지훈(BE) 
* 팀원 : 임휘훈(BE)
* 팀원 : 조성민(FE)

<br/>

### 💻 개발 환경
- **FE** : `React.js`
- **BE** : `Node.js` `Python`
- **IDE** : Visual Studio
- **Framework** : Express.js, Flask
- **Database** : MySQL
- **주요 Library** : Karlo, StableDiffusion, filerobot-image-editor, aws-sdk/client-s3, axios, bootstrap, dotenv


# 직접 담당한 부분 : 

이미지 생성페이지, 이미지 결과 페이지, 이미지 수정 페이지의 UI/UX를 담당하고 Filerobot-Image-Editor 라이브러리를 커스터마이징했습니다.


![이미지생성페이지](https://github.com/pass98/DDal_KKak----/assets/123361606/7fb98e80-f3e8-43a2-a506-9437a198a185)     ![이미지 가이드](https://github.com/pass98/DDal_KKak----/assets/123361606/c9669c04-94b2-4226-9743-6e29bb1900ef)   ![이미지 키워드](https://github.com/pass98/DDal_KKak----/assets/123361606/c51fc6ea-3c54-4473-be55-27c03692859e)


1. 이미지 생성페이지 : 이미지를 생성하는 데 필요한 프롬포트를 입력하는 곳입니다. 가이드 버튼을 클릭하면 사용방법이 슬라이드의 형식으로 나오게 되며, 입력 예시를 돕기 위한 단축키 키워드 버튼,생성하고 싶은 페이지 개수, 입력프롬포트, 제외프롬포트로 나누어져 있습니다. 출력 버튼을 클릭하면 로딩바가 나오며 생성한 이미지에 대한 데이터가 이미지 결과 페이지로 전달됩니다.


![screencapture-localhost-3000-image-result-2023-11-23-15_23_19](https://github.com/pass98/DDal_KKak----/assets/123361606/725d7a2a-10e3-4a9e-a370-fb1434de9f54)


2. 이미지 결과 페이지 : 이미지 생성페이지에서 받은 데이터를 출력합니다. 받은 이미지 개수에 따라 다른 레이아웃이 나오며 나온 사진들 중 수정하고 싶은 이미지를 클릭하면 이미지의 데이터가 이미지 수정 페이지로 전달됩니다.

![screencapture-localhost-3000-image-edit-2023-11-23-15_23_33](https://github.com/pass98/DDal_KKak----/assets/123361606/67791038-c35c-408b-9c7e-60cb5f635d01)

3. 이미지 수정 페이지 : 수정하고 싶은 이미지의 데이터를 전달받아 출력하고 이미지 수정 라이브러리를 통해 이미지에 여러 가지 효과를 주거나 별도의 도형 삽입, 색을 변경 및 부여할 수 있습니다. 저장 버튼을 클릭 시 이미지 사진의 대한 데이터 주소가 유저의 DB에 저장됩니다.


# 라우팅 구성은 이렇게 되어 있습니다.

![이미지 모음](https://github.com/pass98/DDal_KKak----/assets/123361606/f8e2b5f3-b9b8-42bf-80b1-be145eec61dd)  ![이미지 상세](https://github.com/pass98/DDal_KKak----/assets/123361606/9ed19953-9098-45e7-99df-e512ad4787a6)


imgCreate : 이미지 생성에 관련된 페이지입니다. 프롬포트를 통한 이미지 생성 및 저장할 수 있는 이미지 생성페이지 사용자에게 저장되어있는 이미지를 저장 및 공유할 수 있는 마이페이지, 공유된 이미지에 대해 추천을 할 수 있는 이미지 공유 페이지로 구성되어있습니다.


page : 굿즈 상세 페이지로 이동하는 라우터입니다. 클릭시 굿즈의 상세 정보를 확인하고 리뷰를 확인하거나 평가 기능을 구현했습니다.


![굿즈 주문](https://github.com/pass98/DDal_KKak----/assets/123361606/b8e11e4e-6077-4cd6-b324-968c1db996e9)  ![굿즈커스텀](https://github.com/pass98/DDal_KKak----/assets/123361606/91ef04dc-3d22-4488-9ccd-5026634bf2ce)
paymentGoods : 굿즈 구매 페이지입니다. 굿즈를 장바구니에 담거나 굿즈를 직접 구매할 수 있는 기능을 구현했습니다.

socialLogin : 소셜 로그인을 담당하는 페이지입니다. 카카오, 구글, 네이버의 소셜로그인을 가져왔습니다.

socketRoute : socket모듈을 이용하여 이미지 생성 대기열을 처리합니다.


![마이페이지 내정보](https://github.com/pass98/DDal_KKak----/assets/123361606/e1788c62-6c21-4ca5-9eeb-47bce9ad678b)

user : 회원가입과 유저의 정보를 관리하는 라우터입니다.
