<template>
  <section class="technique">
    <div class="text">
      <div class="trademark">
        <h2>Trademark <span>Technique</span></h2>
        <p>My Technique</p>
        <button class="learn-more-btn">
          Learn More
          <svg class="arrow-icon" viewBox="0 0 24 24">
            <path d="M7 17L17 7M17 7H9M17 7V15" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
          </svg>
        </button>
      </div>

      <p class="description">
        For aspiring golf enthusiasts, gain insights<br/> into Brooke eagle-eye swing mechanics<br/>
        and training routines. Discover the artistry<br/> behind a powerful drive and the finesse<br/>
        required for a precision putt.
      </p>

      <p class="sub-description">
        For aspiring golf enthusiasts,<br/> insights into Brooke eagle-eye swing<br/> mechanics
        and routines.
      </p>
    </div>

    <div class="video-area">
      <div class="portrait">
        <img src="@/assets/images/about.webp" alt="Portrait" />
      </div>

      <div class="video">
        <img src="@/assets/images/video.webp" alt="Golf technique" />
        <div class="play-btn">▶</div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.technique {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #d6e02a; 
  padding: 180px 70px;
  gap: 3rem;

  .text {
    flex: 1;

    .trademark {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
    }

    h2 {
      font-size: 6.5rem;
      font-weight: 700;
      line-height: 0.9;
      letter-spacing: -3px;
      margin-bottom: 1rem;
      text-align: right;
    }

    p {
      max-width: 420px;
      margin-bottom: 2rem;
    }

    .sub-description {
      text-align: right;
    }
  }

  .learn-more-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 26px;
    border: 2px solid #000;
    border-radius: 40px;
    font-weight: 600;
    background: transparent;
    cursor: pointer;
    transition: 0.3s ease;

    &:hover {
      background: #000;
      color: #f3f927;
    }

    .arrow-icon {
      width: 20px;
      transition: 0.3s;
    }

    &:hover .arrow-icon {
      transform: translate(3px, -3px);
    }
  }

  .video-area {
    flex: 1;
    position: relative;
    text-align: right;

    .portrait {
      position: absolute;
      top: -90px;
      right: -80px;
      width: 180px;
      height: auto;
      z-index: 5;
      img {
        width: 100%;
      }
    }

    .video {
      position: relative;
      img {
        width: 100%;
        display: block;
      }

      .play-btn {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 4rem;
        background: rgba(255, 255, 255, 0.14);
        color: #fff;
        border-radius: 50%;
        border: 2px solid white;
        width: 150px;
        height: 150px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
      }
    }
  }

 
}




@media (max-width: 1024px) {
  .technique {
    flex-direction: column;
    padding: 120px 50px;
    text-align: center;

    .text {
      .trademark {
        align-items: center;
      }

      h2 {
        text-align: center;
        font-size: 4.5rem;
      }

      .description {
        text-align: center;
      }

      .sub-description {
        display: none; 
      }
    }

    .video-area {
      margin-top: 80px;
      text-align: center;

      .portrait {
        position: static;
        margin-bottom: 20px;
        width: 160px;
      }

      .video img {
        width: 90%;
        margin: 0 auto;
      }
    }
  }
}


@media (max-width: 600px) {
  .technique {
    padding: 70px 25px;
    gap: 2rem;

    .text {
      text-align: center;

      h2 {
        font-size: 3rem;
        line-height: 1.1;
        letter-spacing: -1px;
      }

      .description {
        display: none; 
      }

      .sub-description {
        display: block; 
        text-align: center;
        font-size: 0.95rem;
        line-height: 1.5;
      }

      .learn-more-btn {
        width: 100%;
        justify-content: center;
        padding: 14px;
      }
    }

    .video-area {
      margin-top: 40px;

      .portrait {
        width: 130px;
      }

      .video img {
        width: 100%;
      }

      .video .play-btn {
        width: 80px;
        height: 80px;
        font-size: 2rem;
      }
    }
  }
}

</style>
