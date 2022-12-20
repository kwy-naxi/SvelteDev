<script>
  // 이메일과 비밀번호를 저장할 변수 선언
  let email = "";
  let password = "";

  // 로그인 버튼을 눌렀을 때 실행할 함수
  function handleLogin() {
    // 사용자의 이메일과 비밀번호를 검사하는 API를 호출하고,
    // 로그인이 성공하면 사용자를 로그인 후 페이지로 리다이렉트합니다.
  }
</script>

<!-- 이메일과 비밀번호 입력 양식을 구현 -->
<form on:submit|preventDefault={handleLogin}>
  <label>
    이메일:
    <input type="email" bind:value={email} />
  </label>
  <label>
    비밀번호:
    <input type="password" bind:value={password} />
  </label>
  <button type="submit">로그인</button>
</form>
