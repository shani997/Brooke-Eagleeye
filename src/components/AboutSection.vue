<template>
  <section class="about">
    <div class="about-text">
    <p>About Me</p>
      <h2>Who is <span>Brooke</span></h2>
      <p>
        Discover the story behind the swing.  
        Brooke Eagleeye is more than just a golfer; they are a strategist, a competitor, and a relentless pursuer of perfection.
      </p>
      
  <button class="learn-more-btn">
  Learn More
  <svg class="arrow-icon" viewBox="0 0 24 24">
    <path d="M7 17L17 7M17 7H9M17 7V15" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
  </svg>
</button>



    </div>

    <div class="about-image">
      <img class="main-image" src="@/assets/images/golf-club-ball.webp" alt="Golf club and ball" />
      <img class="portrait" src="@/assets/images/about.webp" alt="Brooke portrait" />
    </div>
  </section>
</template>

<style>
body {
  margin: 0 !important;
  padding: 0 !important;
}
</style>


<style scoped lang="scss">


.about {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  background: #d6e02a;
  width: 100%;           
  box-sizing: border-box;
  padding: 2rem 5%;      
  font-family: 'Poppins', sans-serif; 
  

  .about-text {
    flex: 1;

    h2 {
      font-size: 7rem;
      font-weight: 700;
        line-height: 0.9;      
        letter-spacing: -3px;
        text-align: right;
    }

    p {
      margin: 1.5rem 0;
      max-width: 450px;
      line-height: 1.7;
      font-size: 1rem;
    }

 
  }
.learn-more-btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;

  padding: 12px 26px;
  background: transparent;
  border: 2px solid #000;
  border-radius: 40px;
  font-weight: 600;
  color: #000;
  cursor: pointer;
  transition: 0.3s ease;
}

.learn-more-btn:hover {
  background: #000;
  color: #f3f927;
  border-color: #000;
}


.arrow-icon {
  width: 20px;
  height: 20px;
  transition: 0.3s;
}

.learn-more-btn:hover .arrow-icon {
  transform: translate(3px, -3px);
}


  .about-image {
    flex: 1;
    position: relative;
    text-align: right;

    .main-image {
      width: 60%;
     
    }

    .portrait {
      width: 170px;
      
      position: absolute;
      bottom: -20px;
      left: 160px;
      
    }
  }

 
}




@media (max-width: 992px) {
  .about {
    padding: 2rem 3%;
    flex-direction: column;
    text-align: center;

    .about-text {
      h2 {
        font-size: 5rem;
        text-align: center;
      }

      p {
        margin: 1rem auto;
      }

      .learn-more-btn {
        margin: 1.5rem auto 0;
      }
    }

    .about-image {
      text-align: center;
      margin-top: 2rem;

      .main-image {
        width: 75%;
      }

      .portrait {
        left: 50%;
        transform: translateX(-50%);
        bottom: -10px;
      }
    }
  }
}


@media (max-width: 600px) {
  .about {
    padding: 2rem 1.5rem;

    .about-text {
      h2 {
        font-size: 3rem;
        line-height: 1.1;
        letter-spacing: -1px;
        text-align: center;
      }

      p {
        max-width: 100%;
        font-size: 0.95rem;
      }
    }

    .about-image {
      .main-image {
        width: 95%;
      }

      .portrait {
        width: 130px;
        bottom: -8px;
      }
    }

    .learn-more-btn {
      width: 100%;
      justify-content: center;
      padding: 14px;
    }
  }
}

</style>
