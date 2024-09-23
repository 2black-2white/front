<script>
  let studentId = '';
  let password = '';
  
  const handleLogin = () => {
    console.log("로그인 버튼 클릭", { studentId, password });
  };
</script>

<style>
  @import url('https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css');

  .login-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #15171E;
    color: white;
    font-family: 'Pretendard', sans-serif; 
  }

  .login-box {
    width: 320px;
    padding: 30px;
    background-color: #15171E;
  }

  h1 {
    text-align: left;
    margin-bottom: 20px;
    font-size: 24px;
    transform: translateX(-50px); 
  }

  .input-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  input {
    width: 400px;
    padding: 10px;
    margin-bottom: 15px;
    border-radius: 5px;
    background-color: #1D1F29;
    color: white;
    font-size: 14px;
    border: none; 
  }

  input:focus {
    outline: none; 
  }

  .login-button {
    width: 100%;
    padding: 10px;
    background-color: #1D1F29;
    border: none;
    border-radius: 5px;
    color: white;
    font-size: 16px;
    cursor: pointer;
  }

  .register-link {
    margin-top: 15px;
    text-align: center;
    color: #8F8F8F;
    font-size: 14px;
  }

  .register-link a {
    color: #FFFFFF;
    text-decoration: none;
  }

  .register-link a:hover {
    text-decoration: underline;
  }
</style>

<div class="login-container">
  <div class="login-box">
    <h1>로그인</h1>
    <div class="input-container">
      <input 
        type="text" 
        placeholder="학번을 입력해주세요." 
        bind:value={studentId} />
      <input 
        type="password" 
        placeholder="비밀번호를 입력해주세요." 
        bind:value={password} />
    </div>
    <button class="login-button" on:click={handleLogin}>로그인</button>
    <div class="register-link">
      아직 가입하지 않았다면 <a href="/register">회원 가입 하기</a>
    </div>
  </div>
</div>
