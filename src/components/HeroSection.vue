<template>
  <div class="page-wrapper">
    <header class="nav">
      <div class="logo">be</div>

    
      <button
        class="hamburger"
        :aria-expanded="isOpen.toString()"
        aria-label="Toggle menu"
        @click="toggleMenu"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>

     
      <nav :class="['menu', { open: isOpen }]" @click.self="closeMenu">
        <a href="#">About <span><br />Me</span></a>
        <a href="#">Highlight <span><br />Career</span></a>
        <a href="#">Partner & <span><br />Events</span></a>
        <a href="#">Contact <span><br />Me</span></a>
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
  data() {
    return {
      isOpen: false,
    };
  },
  mounted() {
  
    window.addEventListener('resize', this.handleResize);
  },
  beforeUnmount() {
   
    window.removeEventListener('resize', this.handleResize);
  },
  
  beforeDestroy() {
    if (typeof window !== 'undefined') {
      window.removeEventListener('resize', this.handleResize);
    }
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    closeMenu() {
      this.isOpen = false;
    },
    handleResize() {
      
      if (window.innerWidth > 900 && this.isOpen) {
        this.isOpen = false;
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
  position: absolute;
  width: 100%;
  top: 0;
  z-index: 50;
  background-color: #2bb7f5;

  .logo {
    font-weight: 800;
    font-size: 2rem;
    color: #f3f927;
    z-index: 60;
  }

  .nike-logo {
    width: 90px;
    z-index: 60;
  }


  .menu {
    display: flex;
    gap: 5rem;
    align-items: center;
    z-index: 55;

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
}


.hamburger {
  display: none; 
  background: transparent;
  border: none;
  padding: 0;
  margin-left: 1rem;
  cursor: pointer;
  z-index: 200; 
  display: inline-flex;
  flex-direction: column;
  gap: 6px;
  align-items: center;
  justify-content: center;

  span {
    display: block;
    width: 28px;
    height: 3px;
    background: #f6d84a; 
    border-radius: 2px;
    transition: transform 0.25s ease, opacity 0.25s ease;
  }
}


@media (max-width: 900px) {
  .nav {
    padding: 1rem 1.5rem;

    .nike-logo {
      display: none; 
    }

    .menu {
     
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      right: 0;
      background: #2bb7f5;
      flex-direction: column;
      text-align: center;
      padding: 1.2rem 0;
      gap: 1.2rem;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
      z-index: 100;
    }

    
    .menu.open {
      display: flex;
    }

   
    .hamburger {
      display: inline-flex;
    }
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

.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  cursor: pointer;
  z-index: 100;

  span {
    width: 28px;
    height: 3px;
    background: #f6d84a; 
    transition: 0.3s ease;
  }
}

@media (max-width: 900px) {
  .menu {
    position: absolute;
    top: 80px;
    right: 0;
    background: #2bb7f5;
    width: 100%;
    display: none;
    flex-direction: column;
    text-align: center;
    padding: 1.5rem 0;
    gap: 1.8rem;
  }

  .menu.open {
    display: flex;
  }

  .hamburger {
    display: flex;
  }

  .nike-logo {
    display: none;
  }
}


@media (max-width: 1024px) {
  .player-card-stack {
    display: none !important;
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
