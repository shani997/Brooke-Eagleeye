<template>
<section class="career">
  <div class="career-header-row">
    <p>My Career</p>
    <h2 class="career-title">Career <span>Highlights</span></h2>
  </div>

  <div class="career-content-row">
    <p class="career-description">
      Explore the trophy-laden journey of Brooke<br /> Eagleeye. From triumphant victories
      on<br /> prestigious courses to the resilience shown in<br /> the face of challenges,
      delve into a career<br /> adorned with achievements, accolades, and<br /> unforgettable moments.
    </p>

    <button class="learn-more-btn">
      Discover More
      <svg class="arrow-icon" viewBox="0 0 24 24">
        <path d="M7 17L17 7M17 7H9M17 7V15" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
      </svg>
    </button>
  </div>

 <div class="career-grid">
 
  <img src="@/assets/images/career5.webp" />

 
  <div class="grid-item highlight-box"></div>

 
  <img src="@/assets/images/career4.webp" />

  
  <img src="@/assets/images/career6.webp" />

  
  <img src="@/assets/images/career2.webp" />
  <img src="@/assets/images/career3.webp" />

 
  <div class="grid-item highlight-box">
  <span class="year">2024</span>
  <svg class="arrow" viewBox="0 0 24 24">
    <path d="M7 17L17 7M17 7H9M17 7V15" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round"/>
  </svg>
  <span class="wgc-text">WGC</span>
</div>

  <img src="@/assets/images/career1.webp" />
</div>

</section>



</template>

<style scoped lang="scss">
.career {
  background: #d6e02a;
  padding: 100px 80px;

  
  .career-header-row {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 2rem;

    .section-label {
      font-size: 0.9rem;
      font-weight: 600;
    }

    .career-title {
       font-size: 7rem;
      font-weight: 700;
        line-height: 0.9;      
        letter-spacing: -3px;
        text-align: right;

      span {
        display: block;
      }
    }
  }

 
  .career-content-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 40px;
    flex-wrap: wrap;

    .career-description {
      flex: 1;
      max-width: 600px;
      line-height: 1.5;
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

 
  .career-grid {
    margin-top: 5rem;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    

    

    img {
      width: 100%;
      
    }

     .highlight-box {
    position: relative;
    
    min-height: 220px;
    padding: 20px;
    display: flex;
    justify-content: flex-start; 
    align-items: flex-end;     

    .year {
      position: absolute;
      top: 12px;
      left: 12px;
      font-size: 0.9rem;
      font-weight: 600;
      color: #000;
    }

    .arrow {
      position: absolute;
      top: 12px;
      right: 12px;
      width: 48px;
      height: 48px;
      color: #000;
    }

    .wgc-text {
      font-size: 3rem;
      font-weight: 700;
      color: #000;
      letter-spacing: -1px;
      text-align:left;
    }
  }
  }
}

@media (max-width: 1200px) {
  .career {
    padding: 80px 50px;

    .career-title {
      font-size: 5rem !important;
    }

    .career-description {
      max-width: 500px;
    }
  }
}

@media (max-width: 992px) {
  .career {
    padding: 70px 40px;

    .career-header-row {
      flex-direction: column;
      align-items: center;
      text-align: center;

      .career-title {
        text-align: center !important;
        font-size: 4rem !important;
      }
    }

    .career-content-row {
      flex-direction: column;
      align-items: center;
      text-align: center;

      .career-description {
        margin: 0 auto;
      }

      .learn-more-btn {
        margin-top: 20px;
      }
    }

    .career-grid {
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }
  }
}

@media (max-width: 768px) {
  .career {
    padding: 60px 30px;

    .career-title {
      font-size: 3rem !important;
      line-height: 1.1;
    }

    .career-grid {
      grid-template-columns: repeat(2, 1fr);
    }

    .highlight-box .wgc-text {
      font-size: 2.2rem;
    }
  }
}

@media (max-width: 480px) {
  .career {
    padding: 50px 20px;

    .career-title {
      font-size: 2.3rem !important;
      text-align: left;
    }

    .career-description br {
      display: none; 

    }

  .career {
    .career-header-row,
    .career-content-row {
      text-align: center;
      align-items: center;
    }

    .career-description {
      margin: 0 auto;
    }
    }
    .career-grid {
      grid-template-columns: 1fr;
      gap: 15px;
    }

    .highlight-box {
      min-height: 180px;

      .wgc-text {
        font-size: 1.8rem;
      }

      .arrow {
        width: 34px;
        height: 34px;
      }
    }

    .learn-more-btn {
      width: 100%;
      justify-content: center;
    }
  }
}


</style>
