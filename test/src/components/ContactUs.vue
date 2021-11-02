<template>
  <div id="contact" class="container">
    <div class="search">
      <div class="form-control">
        <input
          type="text"
          id="search"
          placeholder="Search"
          style="font-family: Poppins, FontAwesome"
        />
      </div>
    </div>
    <section class="contact">
      <div>
        <img src="@/assets/svg/phone.svg" alt="phone number" />
        <p>111 222 333</p>
      </div>
      <div class="frame">
        <img src="@/assets/svg/mail.svg" alt="e-mail" />
        <p>index@gmail.com</p>
      </div>
      <div>
        <img src="@/assets/svg/street.svg" alt="street" />
        <p>123 Street Block</p>
      </div>
    </section>
    <div class="form">
      <div class="wrapping">
        <form id="my-form" @submit.prevent="submitForm">
          <div class="wrapper">
            <div class="form-control">
              <h1>Feedback</h1>
              <input
                type="text"
                id="yourname"
                placeholder="Your Name"
                style="font-family: Poppins, FontAwesome"
              />
            </div>
            <div class="form-control">
              <input
                type="email"
                id="email"
                placeholder="Email"
                style="font-family: Poppins, FontAwesome"
              />
            </div>
            <div class="message">
              <div class="form-control">
                <textarea
                  id="message"
                  rows="13"
                  placeholder="Message"
                  maxlength="500"
                  style="font-family: Poppins, FontAwesome"
                />
              </div>
            </div>
          </div>
          <div class="map"></div>
        </form>
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
  min-height: 130vh;
  background-color: #ffffff;
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
  .search {
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
        width: 850px;
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
  .contact {
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    width: 80%;
    padding: 2% 2%;
    div {
      width: 30%;
      margin-top: 1%;
      padding: 2% 0;

      img {
        display: block;
        margin: 0 auto;
      }
      p {
        text-align: center;
        margin-top: 10%;
        font-size: 1.6rem;
        color: black;
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
    .message {
      width: 100%;
      textarea {
        padding: 10%;
      }
    }
  }
  button {
    cursor: pointer;
    color: white;
    font-size: 1.8rem;
    font-weight: 500;
    display: block;
    margin: 2% auto;
    padding: 1.5% 7%;
    // margin-bottom: 100px;
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
