<template>
  <section class="contact-hero">
    <div class="contact-content">
      <h1 class="contact-title">
        CONTACT <span>ME</span>
      </h1>
    </div>

    
  </section>
</template>

<style scoped lang="scss">
.contact-hero {
  background: #2bb7f5;
  padding: 100px 70px;
  text-align: center;
  color: #111;
  position: relative;
  overflow: hidden;

  &::before {
    content: "";
    background: url("@/assets/images/contact-object.webp") center/contain no-repeat;
    position: absolute;
    top: 0;
    left: 50%;
    width: 550px;
    height: 550px;
    transform: translateX(-50%);
    opacity: 1;
    z-index: 1;
  }

  .contact-content {
    position: relative;
    z-index: 2;
  }

  .contact-title {
    font-size: 7rem;
    font-weight: 700;
    line-height: 0.9;
    letter-spacing: -3px;
    color: #d6e02a;

    span {
      display: block;
      line-height: 0.9;
    }
  }

  .contact-form-wrap {
    margin-top: 18rem;
    z-index: 3;
    position: relative;

    p {
      font-size: 1.1rem;
      margin-bottom: 1.5rem;
      color: #222;
    }

    form {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;

      input,
      textarea {
        width: 80%;
        max-width: 480px;
        background: #fff;
        border-radius: 12px;
        border: none;
        padding: 1rem;
        font-size: 1rem;
      }

      button {
        background: #e5ff42;
        color: #111;
        border: 2px solid #000;
        border-radius: 50px;
        font-weight: 700;
        cursor: pointer;
        padding: 0.9rem 2.5rem;
        transition: 0.2s;

        &:hover {
          transform: translateY(-2px);
          box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
        }
      }
    }
  }
}


@media (max-width: 1024px) {
  .contact-hero {
    padding: 80px 40px;

    &::before {
      width: 430px;
      height: 430px;
    }

    .contact-title {
      font-size: 5rem;
    }

    .contact-form-wrap {
      margin-top: 14rem;
    }
  }
}


@media (max-width: 600px) {
  .contact-hero {
    padding: 60px 25px;

    &::before {
      width: 300px;
      height: 300px;
      opacity: 0.6;
    }

    .contact-title {
      font-size: 3.2rem;
      letter-spacing: -1px;
    }

    .contact-form-wrap {
      margin-top: 8rem;

      form input,
      form textarea {
        width: 100%;
      }

      form button {
        width: 100%;
      }
    }
  }
}
</style>

