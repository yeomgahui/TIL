좋은 사이트 
https://codeburst.io/localstorage-vs-cookies-all-you-need-to-know-about-storing-jwt-tokens-securely-in-the-front-end-70dc0a9b3ad3


1. 리프레시 토큰은 HTTP ONLY SECURE 쿠키에 저장하자.

2. 액세스 토큰은 프로그램상 자바스크립트 로컬 변수에 저장하고, http 헤더에 bearer 토큰으로 담아서 매 요청마다 보내도록 하자.

3. 로컬스토리지는 사용하지 말자. (보안에 매우 취약)

