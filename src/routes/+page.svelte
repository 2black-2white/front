<script>
  let studentId = '';
  let password = '';
  
  const handleLogin = () => {
    console.log("로그인 버튼 클릭", { studentId, password });
  };

  const handleSignup = () => {
    window.location.href = '/signup'; // Redirect to /signup
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
    text-align: center; 
    margin-bottom: 20px;
    font-size: 50px; 
  }

  .login-button {
    width: 200px;
    padding: 10px;
    background-color: #1D1F29;
    border: none;
    border-radius: 5px;
    color: white;
    font-size: 16px;
    cursor: pointer;
    margin-left: 60px;
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
    <h1>환영합니다</h1>
    <button class="login-button" on:click={handleSignup}>회원가입</button>
    <div class="register-link">
      이미 가입한 사용자라면<a href="/signin"> &nbsp 로그인 하기</a>
    </div>
  </div>
</div>
