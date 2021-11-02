<template>
  <div id="login" class="container">
    <div class="login-form">
      <div class="email">
        <div class="form-control">
          <input
            type="text"
            id="email"
            placeholder="Email"
            style="font-family: Poppins, FontAwesome"
          />
        </div>
      </div>
      <div class="email">
        <div class="form-control">
          <input
            type="text"
            id="email"
            placeholder="Email"
            style="font-family: Poppins, FontAwesome"
          />
        </div>
      </div>
      <div class="button"><button type="submit" form="my-form">Send Message</button></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  max-width: 100vw;
  min-height: 5vh;
  header {
    text-align: center;
    color: black;
    font-size: 5rem;
    font-weight: bold;
    padding-top: 5%;
  }
  h1 {
    font-size: 1.8rem;
    color: black;
    text-align: center;
  }
  .login-form {
    display: flex;
    gap: 20px;
  }
  .email {
    position: relative;
    left: 200px;
    top: 20px;
    .form-control {
      margin: 0.5rem 0;
      width: 80%;
      label {
        display: block;
        font-size: 1.8rem;
        font-weight: 400;
        margin-bottom: 0.3rem;
      }
      input,
      textarea {
        background-color: #f1f1f1;
        border: none;
        border-radius: 10px;
        font-size: 1.4 rem;
        width: 350px;
        min-height: 4rem;
        resize: none;
        padding-left: 5%;
      }
      .invalid {
        label {
          color: red;
        }
        input {
          border: 1px solid red;
        }
        ::-webkit-input-placeholder {
          color: red;
        }
      }
      input::-webkit-outer-spin-button,
      input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
      }
      p {
        margin-top: -13%;
        color: red;
      }
    }
  }

  .form {
    border: 1px solid #eaeaea;
    border-radius: 10px;
    margin: 0 auto;
    width: 90%;
    display: flex;
    flex-direction: column;
    form {
      display: flex;
      flex-wrap: wrap;
      margin: 2% 5%;
      justify-content: space-around;
      .wrapper {
        width: 50%;
        margin-right: 450px;
      }
      .form-control {
        margin: 0.5rem 0;
        width: 100%;
        label {
          display: block;
          font-size: 1.8rem;
          font-weight: 500;
          margin-bottom: 0.3rem;
        }
        input,
        textarea {
          background-color: #f1f1f1;
          border: none;
          border-radius: 10px;
          font-size: 1.4 rem;
          width: 90%;
          min-height: 4rem;
          margin-bottom: 12%;
          resize: none;
          padding-left: 5%;
        }
        .invalid {
          label {
            color: red;
          }
          input {
            border: 1px solid red;
          }
          ::-webkit-input-placeholder {
            color: red;
          }
        }
        input::-webkit-outer-spin-button,
        input::-webkit-inner-spin-button {
          -webkit-appearance: none;
          margin: 0;
        }
        p {
          margin-top: -13%;
          color: red;
        }
        h1 {
          font-size: 20px;
          font-weight: 700;
        }
      }
    }
  }
  button {
    cursor: pointer;
    color: white;
    font-size: 1.3rem;
    font-weight: 500;
    display: block;
    margin: 2% auto;
    padding: 1% 5%;
    margin-left: 200px;
    margin-top: 26px;
    border: none;
    border-radius: 5px;
    line-height: 28px;
    background: rgb(255, 154, 98);
    background: linear-gradient(
      90deg,
      rgba(255, 154, 98, 1) 0%,
      rgba(255, 114, 121, 1) 50%,
      rgba(255, 68, 147, 1) 100%
    );
  }
}
@media screen and (max-width: 1024px) {
  .container {
    min-height: 95vh;
    .contact {
      width: 70%;
      margin-bottom: 10%;
      div {
        margin: 2% auto;
      }
    }
    .form {
      width: 90%;
    }
  }
}

@media screen and (max-width: 768px) {
  .container {
    min-height: 95vh;
    .contact {
      width: 70%;
      margin-bottom: 10%;
      div {
        margin: 2% auto;
      }
    }
    .form {
      width: 90%;
    }
  }
}

@media screen and (max-width: 375px) {
  .container {
    min-height: 70vh;
    .contact {
      width: 70%;
      margin-bottom: 10%;
      div {
        margin: 2% auto;
      }
    }
    .form {
      width: 90%;
    }
  }
}
</style>
