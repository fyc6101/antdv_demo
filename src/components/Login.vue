<template>
  <div class="content">
    <div class="login-ct">
      <div class="title">Login Demo</div>
      <div class="login">
        <div class="login-icon">
          <img class="vue-logo" alt="Vue logo" src=".././assets/logo.png" />
        </div>
        <div class="login-item">
          <a-form
            id="components-form-demo-normal-login"
            :form="form"
            class="login-form"
            @submit="handleSubmit"
          >
            <a-form-item>
              <a-input
                v-decorator="[
                  'userName',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your username!',
                      },
                    ],
                  },
                ]"
                placeholder="Username"
              >
                <a-icon
                  slot="prefix"
                  type="user"
                  style="color: rgba(0, 0, 0, 0.25)"
                />
              </a-input>
            </a-form-item>
            <a-form-item>
              <a-input
                v-decorator="[
                  'password',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your Password!',
                      },
                    ],
                  },
                ]"
                type="password"
                placeholder="Password"
              >
                <a-icon
                  slot="prefix"
                  type="lock"
                  style="color: rgba(0, 0, 0, 0.25)"
                />
              </a-input>
            </a-form-item>
            <a-form-item>
              <a-checkbox
                v-decorator="[
                  'remember',
                  {
                    valuePropName: 'checked',
                    initialValue: true,
                  },
                ]"
              >
                Remember me
              </a-checkbox>
              <a class="login-form-forgot" href=""> Forgot password </a>
              <a-button
                type="primary"
                html-type="submit"
                class="login-form-button"
              >
                Log in
              </a-button>
              Or
              <a href=""> register now! </a>
            </a-form-item>
          </a-form>
        </div>
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
    // text-align: center;
    background-color: #ffffff;
    height: 350px;
    width: 800px;
    border-radius: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .title {
      font-size: 36px;
      height: 50px;
      margin-bottom: 8px;
    }

    .login {
      display: flex;
      align-items: flex-end;

      .login-icon {
        padding: 0 26px 44px 0;
        .vue-logo{
          height: 240px;
        }
      }

      .login-item {
        width: 300px;
      }
    }
  }
}

#components-form-demo-normal-login .login-form-forgot {
  float: right;
}
#components-form-demo-normal-login .login-form-button {
  width: 100%;
}
</style>
