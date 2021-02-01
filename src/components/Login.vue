<template>
  <div class="content">
    <div class="login-ct">
      <div class="title">Login Demo</div>
      <div class="login">
        <div class="login-icon"></div>
        <img alt="Vue logo" src=".././assets/logo.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.content {
  height: 100%;
  background-color: #f5f7fd;
  display: flex;
  align-items: center;
  justify-content: center;

  .login-ct {
    text-align: center;
    background-color: #ffffff;
    height: 350px;
    width: 600px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .title {
      font-size: 30px;
    }

    .login{
      display: flex;
      
    }
  }
}
</style>
