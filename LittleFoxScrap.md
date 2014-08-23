#### Little Fox 동화 내용을 Scrap하기

##### 로그인하기
Little Fox의 로그인부분 간략화한 HTML코드는 다음과 같다.
``` html
<div class="login_box_form">
    <form id="frmLogin" name="frmLogin" target="frmLoginTarget" action="https://www.littlefox.co.kr/ko/login/auth_process" method="post" onsubmit="return login_form_proc();">

	<input type="hidden" name="mode" value="">
    <input type="hidden" name="fail_url" id="fail_url" value="/ko" >
    <input type="text" class="login_username dis" name="loginid" id="loginid" value="hyde1004" >
    <input type="password" class="login_password" name="loginpw" id="loginpw" value="LLpEkZ" >
    <input type="hidden" name="base_pw" value="LLpEkZ">

	</form>
</div>
```

위의 코드를 더 단순화 시키면 다음과 같다.
``` html
<!-- 
	name="" : 항목
    value="" :항목의 값 
    class, id : css 항목
    
    onsubmit, target : javascript로 새챙을 열어, id, pw를 전송하는 방법
    onsubmit : 입력 양식의 데이터를 서버로 보낼 때 실행되는 이벤트 핸들러
    target : 입력 양식의 데이터를 서버로 보낸 후에 받아 보는 결과를 다른  윈도우에서 보고 싶은 경우에 지정
-->

<form action="서버로 보낼 URL" method="전송방법">
	<input type="text" name="" value="">   <!-- 문자 입력 박스 -->
    <input type="password" name="" value="">   <!-- 암호 입력 박스 -->
</form>
```

성공여부를 확인하기 위한 URL. 다음 URL이 읽을수 있으면 성공이다.
http://www.littlefox.co.kr/ko/supplement/org/C0003640
