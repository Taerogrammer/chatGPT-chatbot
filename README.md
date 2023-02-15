# ChatGPT-chatbot
2022 SKKU 산학 협력 프로젝트 / Talking NPC / 사이드 프로젝트

<br>

> 작년에 진행한 산학 협력 프로젝트 관련하여 Talking NPC/ WikiChatbot의 BERT model을 GPT-3 model로의 시연을 부탁하셔서 제작하였습니다.

> GPT-3 model은 최근에 엄청난 화제가 되고 있는 '[ChatGPT](https://openai.com/blog/chatgpt/)'에 사용되는 모델로써, 뛰어난 문장 생성 능력을 보여주는 모델입니다.

> GPT-3 model 중 가장 최신 버전인 'text-davinci-003' model을 사용하였고, ChatGPT는 이 model을 fine-tuning하여 만들어졌다고 합니다.

<br>

※ 시간 관계 상 https://www.youtube.com/watch?v=1ppzNLfUwTY 의 구현 방법을 이용하였습니다. ※

<br>
<br>
<br>

## Framework

Vue / Express(node.js) / AWS EC2 (Ubuntu)


<br>
<br>
<br>

## 설치 방법

### Prerequisites

- NPM, Vue, nodejs 등을 설치해야 합니다.

- 콘솔 창에 다음 명령어를 실행하여 필요한 패키지들을 설치해줍니다.

<br>

- install NPM

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

- install node.js

```sh
sudo yum install nodejs
```

- install yarn

```sh
npm install -g yarn
```

- install vue

```sh
npm install vue
```



### Clone Repository

```sh
git clone https://github.com/Taerogrammer/chatGPT-chatbot.git
```

- vue 실행하기 위해 설치

```sh
npm init vue@latest
```

<br>
<br>
<br>

## 파일 구조 및 실행 방법

- 트리 안에 여러 폴더(패키지 등)가 매우 많기 때문에, 핵심적인 폴더 위주로 작성하였습니다. 

```
chatGPT
 ┣ frontend
 ┃ ┣ index.html
 ┃ ┣ node_modules
 ┃ ┣ package.json
 ┃ ┣ public
 ┃ ┗ src
 ┃ ┃ ┗ App.vue
 ┃ ┃ ┗ main.js
 ┃ ┃ ┗ assets
 ┃ ┃ ┗ components
 ┃ ┃ ┃ ┗ Chat.vue
 ┃ ┃ ┗ router
 ┃ ┣ yarn.lock
 ┃ ┃ ┗ views
 ┃ ┃ ┃ ┗ HomeView.vue
 ┣ backend
 ┃ ┣ node_modules
 ┃ ┣ package.json
 ┃ ┣ yarn.lock
 ┃ ┗ server.js
 ┣ node_modules
```

- frontend
  - Chat.vue : Chatting과 관련한 component입니다.
  - HomeView.vue : 웹사이트 화면 및 chatting을 받아오는 기능이 있습니다.
  
- backend 
  - server.js : API를 요청하고 서버를 실행하는 파일입니다.
  
  
※ 이 파일을 clone하여 진행할 경우, 본인의 API key가 필요하기 때문에, 

[openAI](https://platform.openai.com/overview)에서 API key를 인증받고, backend/.env 파일에 본인의 API key를 작성해야합니다.

만약 API key를 발급받았는데, 실행이 되지 않는 경우(error 429), 본인의 카드를 설정해놓으면 작동할 것입니다. (2월 15일 기준)

  

<br>
<br>

- 실행 방법
 
 - frontend와 backend 파일을 각각 실행해야 하기 때문에, 두 개의 터미널을 열어줍니다.
 <br>
 
 - frontend
   - frontend 디렉토리로 이동한 뒤, 다음과 같은 명령어를 실행해줍니다.
   
   ```
   npm run dev -- --host
   ```
   
 - backend
   - backend 디렉토리로 이동한 뒤, 다음과 같은 명령어를 실행해줍니다.
   
   ```
   node server.js
   ```
   
   
 ## 사용 예제 
 
 - 만약 위의 과정을 실행하였다면, frontend 및 backend가 실행되고, 다음과 같은 화면이 나타날 것입니다.
 <br>
 
 <img width="1000" alt="image" src="https://user-images.githubusercontent.com/104834390/218910209-5f73a02b-f203-4bec-b38b-19f78b696c3c.png">
 
 - 이 화면에서 질문을 한다면, 질문에 대한 응답을 해줍니다. 
 
<img width="1000" alt="image" src="https://user-images.githubusercontent.com/104834390/218910308-ca0bf1e8-bf66-4358-9403-9a4c570cd93a.png">


<br>
<br>

### AWS 배포 주소 

43.201.60.135:5173



