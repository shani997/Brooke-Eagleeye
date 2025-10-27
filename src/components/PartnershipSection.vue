<template>
  <section class="partnership">
    <div class="title-section">
      <div class="content">
        <h2>Partnerships & <span>Events</span></h2>
        <p>My Partnership</p>
        <div class="down-section">
          <button class="learn-more-btn">
            Contact Me
            <svg class="arrow-icon" viewBox="0 0 24 24">
              <path
                d="M7 17L17 7M17 7H9M17 7V15"
                stroke="currentColor"
                stroke-width="2"
                fill="none"
                stroke-linecap="round"
              />
            </svg>
          </button>
          <p>
            Explore Opportunities for collaborations <br /> with brands and events that corporate <br /> share Brooke’s
            passion for excellence <br /> from global tournaments to leading <br /> golf equipment professional partners.
          </p>
        </div>
      </div>
    </div>
    <div class="carousel">
      <div class="carousel-track">
        <div class="slide"><img src="@/assets/images/brooke.webp" alt="Ping" /></div>
        <div class="slide"><img src="@/assets/images/nike.webp" alt="Nike" /></div>
        <div class="slide"><img src="@/assets/images/wilson.webp" alt="Wilson" /></div>
        <div class="slide"><img src="@/assets/images/brooke.webp" alt="Ping" /></div>
        <div class="slide"><img src="@/assets/images/nike.webp" alt="Nike" /></div>
        <div class="slide"><img src="@/assets/images/wilson.webp" alt="Wilson" /></div>
      </div>

      <div class="carousel-dots"></div>
    </div>
  </section>
</template>



<script>
export default {
  data() {
    return {
      currentIndex: 0,
      slides: [],
    };
  },
  mounted() {
    this.slides = Array.from(document.querySelectorAll('.carousel .slide'));
    this.setActiveSlide();
    this.autoMove();
  },
methods: {
  setActiveSlide() {
   
    this.slides.forEach((slide, index) => {
      slide.classList.remove('active', 'prev', 'next');
      
     
      const prevIndex = (this.currentIndex - 1 + this.slides.length) % this.slides.length;
      const nextIndex = (this.currentIndex + 1) % this.slides.length;
      
     
      if (index === this.currentIndex) {
        slide.classList.add('active');
      }
    
      else if (index === prevIndex) {
        slide.classList.add('prev');
      }
     
      else if (index === nextIndex) {
        slide.classList.add('next');
      }
    });
  },
  
  autoMove() {
    setInterval(() => {
      this.currentIndex = (this.currentIndex + 1) % this.slides.length;
      this.setActiveSlide();
      this.updateCarouselPosition();
    }, 3000); 
  },
  
  updateCarouselPosition() {
   
    const offset = -this.currentIndex * 33.33; 
    document.querySelector('.carousel-track').style.transform = `translateX(${offset}%)`;
  }
}


};
</script>







<style scoped lang="scss">
.partnership {
  background: #0b0c10;
  color: $text-light;
  text-align: center;
  padding: 150px 50px;

  .title-section {
    width: 70%;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
  }

  h2 {
    font-size: 7rem;
    font-weight: 700;
    line-height: 0.9;
    letter-spacing: -3px;
    text-align: left;
    color: #d6e02a;
  }

  p {
    margin: 1.2rem auto 2rem;
    max-width: 600px;
    text-align: right;
    color: #d6e02a;
  }

  .down-section {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 40px;
    flex-wrap: wrap;
  }

  .learn-more-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 26px;
    background: transparent;
    border: 2px solid #d6e02a;
    border-radius: 40px;
    font-weight: 600;
    color: #d6e02a;
    cursor: pointer;
    transition: 0.3s ease;
  }

  .learn-more-btn:hover {
    background: #d6e02a;
    color: #000;
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


  .carousel {
    position: relative;
    display: flex;
    justify-content: center;
    overflow: hidden;
    width: 100%;
    margin-top: 30px;
  }

  .carousel-track {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }

  .slide {
    flex: 0 0 33.33%;
    transition: transform 0.3s ease, opacity 0.3s ease;
    opacity: 0.8;
    transform: scale(0.9);
    text-align: center;
  }

  .slide img {
    width: 100%;
    
  }

  .carousel .slide.active {
    transform: scale(1);
    opacity: 1;
  }


  .carousel .slide.prev,
  .carousel .slide.next {
    transform: scale(0.9);
    opacity: 0.8;
  }

  .carousel .slide.active {
    transform: scale(1);
    opacity: 1;
  }

 
  .carousel-dots {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-top: 10px;
  }

  .carousel-dots span {
    width: 10px;
    height: 10px;
    background-color: #d6e02a;
    border-radius: 50%;
    opacity: 0.5;
    transition: opacity 0.3s ease;
    cursor: pointer;
  }

  .carousel-dots .active {
    opacity: 1;
  }
}




@media (max-width: 1024px) {
  .partnership {
    padding: 100px 40px;

    h2 {
      font-size: 4.5rem;
      text-align: center;
    }

    .title-section p {
      text-align: center;
    }

    .down-section {
      flex-direction: column;
      text-align: center;

      p {
        text-align: center;
      }
    }

    .learn-more-btn {
      margin-bottom: 20px;
    }

    /* Show 2 slides */
    .carousel-track {
      transform: translateX(0) !important;
    }

    .slide {
      flex: 0 0 50%;
    }
  }
}


@media (max-width: 600px) {
  .partnership {
    padding: 70px 25px;

    h2 {
      font-size: 2.6rem;
      line-height: 1.1;
      letter-spacing: -1px;
      text-align: center;
    }

    .title-section {
      width: 100%;
    }

    .title-section p {
      max-width: 100%;
      text-align: center;
      margin-top: 10px;
    }

    .down-section {
      flex-direction: column;
      gap: 20px;
      text-align: center;
    }

    .learn-more-btn {
      width: 100%;
      justify-content: center;
      padding: 14px;
    }

   
    .slide {
      flex: 0 0 100%;
      transform: scale(1) !important;
      opacity: 1 !important;
    }

   
    .carousel .slide.prev,
    .carousel .slide.next {
      transform: scale(1) !important;
      opacity: 1 !important;
    }

    .carousel-track {
      transition: transform 0.4s ease;
    }

    .carousel {
      margin-top: 40px;
    }

    .carousel-dots {
      margin-top: 18px;
    }
  }
}


</style>
