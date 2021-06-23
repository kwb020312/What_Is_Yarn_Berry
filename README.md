## What is Yarn Berry

<img src="gitImages\Yarn_Logo.jpg" />

Yarn Berry란 무엇일까?? 학습하는 시간을 가져보겠다.

본 Repository는 Toss 개발자분들이 작성해주신 문서를 보고 참조하였음을 미리 밝힙니다.

<a href="https://toss.tech/article/node-modules-and-yarn-berry">토스 게시물 바로보기</a>

<blockquote cite="https://toss.tech/article/node-modules-and-yarn-berry">
    Yarn Berry는 기존의 “깨져 있는” NPM 패키지 관리 시스템을 혁신적으로 개선합니다.
</blockquote>

## 왜 Yarn Berry를 사용하는가??

현재 NPM은 무겁기로 명성이 자자하며 그렇기에 아래와 같은 이미지가 많은 개발자들의 웃음을 자아내고있다.

<img src="gitImages\Gravity.jpg">

그 만큼 Node_Modules의 용량이 무겁다는 소리이며 이를 개선하고자 Node.js의 취약점을 보안하며 Dino또한 인기를 얻게되었다고 생각한다.

여러가지 이유가 있지만 결론적으로 통합되는 이유는 node_modules 폴더의 용량이 비효율적이게 커져서라고 볼 수 있으며 그렇기에 Yarn Berry를 대체하여 사용한다.

<i>현재 Toss는 대부분의 라이브러리를 대체하여 사용하고 있다.</i>

## Plug n Play

Plug n Play는 이러한 문제들을 예방하고자 출발하게 되었다.

## Plug n Play 활성화

```javascript
// yarn을 설치함
npm i -g yarn
// yarn package 가 설치된 경로로 이동
cd ../path/yarn위치
// 버전을 berry로 설정함
yarn set version berry
```

이제 yarn 으로 패키지를 설치하였을 때 node_modules가 생성되지 않고 의존성 정보를 기록하는 .pnp.cjs파일이 생성되며 이 파일을 조회할 시 어떤 라이브러리에 의존하는지 자세하게 나와있음을 알 수 있다.

평소와 달라지는 점은 pnp를 사용하는 경우 node 는 사용할 수 없고 대신 yarn node를 사용하여야 하며 나머지는 그대로 동작한다.
