<template>
  <div class="page-wrapper">
    <header class="nav">
      <div class="logo">be</div>

      <nav class="menu">
        <a href="#"
          >About <span><br />Me</span>
        </a>
        <a href="#"
          >Highlight <span><br />Career</span></a
        >
        <a href="#"
          >Partner & <span><br />Events</span></a
        >
        <a href="#"
          >Contact <span><br />Me</span></a
        >
      </nav>

      <img class="nike-logo" src="@/assets/images/nike.png" alt="Nike Logo" />
    </header>

    <section class="hero">
      <div class="hero-content">
        <div class="player-cards">
         <div class="player-card-stack">
  
  <div class="player-card top-card">
    <img src="@/assets/images/wilson.webp" alt="Brooke Eagleeye" />
    <h3>Brooke Eagleeye</h3>
    <p>WGC Champions 2025</p>
  </div>

 
  <div class="player-card back-card">
    <img src="@/assets/images/brooke.webp" alt="Brooke Eagleeye" />
    <h3>Brooke Eagleeye</h3>
    <p>WGC Champions 2024</p>
  </div>
</div>

        </div>

        
        <div class="hero-text">
          <h1><span>GOLF</span><br />JOURNEY</h1>
          <p>
            Embark on a journey through the fairways <br />
            and greens with Brooke Eagleeye, a<br />
            dedicated and accomplished <br />professional golfer.
          </p>

          <div class="socials">
            <i class="fa-brands fa-instagram"></i>
            <i class="fa-brands fa-youtube"></i>
            <i class="fa-brands fa-x-twitter"></i>
            <i class="fa-brands fa-tiktok"></i>
          </div>
        </div>

        
       
      </div>
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const hero = document.querySelector('.hero');
      if (window.scrollY > 100) { 
        hero.classList.add('scrolled');
      } else {
        hero.classList.remove('scrolled');
      }
    },
  },
};
</script>


<style scoped lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 6rem;
  background: transparent;
  position: absolute;
  width: 100%;
  top: 0;
  z-index: 20;
  background-color: #2bb7f5;

.hero.scrolled {
  background-color: #2bb7f5;
}

  .logo {
    font-weight: 800;
    font-size: 2rem;
    color: #f3f927;
  }

  .menu {
    display: flex;
    gap: 5rem;

    a {
      color: white;
      font-size: 0.95rem;
      text-decoration: none;
      transition: 0.2s;
      &:hover {
        opacity: 0.8;
      }
    }
  }

  .nike-logo {
    width: 90px;
  }
}


.hero {
 background-color: #2bb7f5; 
  padding: 130px 70px;
  position: relative;
  overflow: hidden;
  transition: background-color 0.3s ease;

  .hero-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3rem;

    .hero-text {
      flex: 1;
      text-align: right;

      h1 {
        font-size: 8rem;
        font-weight: 900;
        line-height: 0.9;
        color: #f3f927;
      }

      p {
        margin: 1.5rem 0;
        color: #fff;
      }

      .hero.scrolled {
  background-color: #a6d8f7 !important; 
}

      .socials {
        margin-top: 1rem;
        display: flex;
        justify-content: flex-end;
        gap: 0.4rem;

        i {
          font-size: 1rem;
          color: white !important;
          cursor: pointer;

          background: #3b3b3b;
          padding: 12px 20px;
          border-radius: 50%;
          display: flex;
          align-items: center;
          justify-content: center;

          transition: 0.3s;

          &:hover {
            background: #555;
            transform: translateY(-3px);
          }
        }
      }
    }

  
    .player-card-stack {
      position: relative;
      width: 220px;
      margin-left: 0.5rem;

      &:hover .back-card {
        z-index: 4;
        transform: rotate(0deg) translate(0px, 0px) scale(1.06);
      }

      &:hover .top-card {
        z-index: 2;
        transform: rotate(24deg) translate(50px, -30px);
      }
    }

    .player-card {
      background: #fff;
      width: 220px;
      padding: 1rem;
      border-radius: 6px;
      box-shadow: 0 8px 18px rgba(0, 0, 0, 0.25);
      text-align: center;
      position: absolute;
      left: 0;
      top: 0;
      transition: 0.35s ease;

      img {
        width: 100%;
        border-radius: 4px;
        margin-bottom: 0.8rem;
      }

      h3 {
        font-size: 1.1rem;
        font-weight: 700;
        color: #000;
      }

      p {
        color: #666;
        font-size: 0.9rem;
      }
    }

    .top-card {
      z-index: 3;
    }

    .back-card {
      z-index: 1;
      transform: rotate(24deg) translate(50px, -30px);
      opacity: 0.9;
    }
  }
}




@media (max-width: 1024px) {
  .nav {
    padding: 1.5rem 3rem;
    .menu {
      gap: 2.5rem;
    }
  }

  .hero {
    padding: 120px 40px;
    .hero-content {
      gap: 2rem;
      .hero-text h1 {
        font-size: 6rem;
      }
    }
  }
}


@media (max-width: 768px) {
  .nav .menu {
    display: none;
  }

  .hero {
    padding: 120px 30px;
    .hero-content {
      flex-direction: column;
      text-align: center;

      .player-cards,
      .player-card-stack {
        margin: 0 auto;
      }

      .hero-text {
        text-align: center;
        margin-top: 2rem;

        h1 {
          font-size: 4.5rem;
        }

        .socials {
          justify-content: center;
        }
      }
    }
  }
}


@media (max-width: 480px) {
  .hero {
    padding: 100px 20px;

    .hero-content .hero-text h1 {
      font-size: 3.2rem;
    }

    .player-card-stack,
    .player-card {
      width: 180px;
    }
  }
}
</style>
