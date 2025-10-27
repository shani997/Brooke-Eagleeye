<template>
  <header class="top-nav">
    <div class="nav-left">
      <span class="logo-be">be</span>
    </div>

  
    <nav class="menu" :class="{ open: isMenuOpen }">
      <a href="#">About <span><br />Me</span></a>
      <a href="#">Highlight <span><br />Career</span></a>
      <a href="#">Partner & <span><br />Events</span></a>
      <a href="#">Contact <span><br />Me</span></a>
    </nav>

    <div class="nav-right">
      <img class="logo-nike" src="@/assets/images/nike-logo.svg" alt="nike logo" />
    </div>

   
    <div class="hamburger" @click="isMenuOpen = !isMenuOpen">
      <span></span><span></span><span></span>
    </div>
  </header>

  <section class="hero-name">
    Brooke Eaaaleeve
  </section>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
};
</script>

<style scoped lang="scss">
.top-nav {
  background: linear-gradient(90deg, #b2391f, #e06a28);
  padding: 1.2rem 3rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;

  .logo-be {
    font-size: 1.8rem;
    font-weight: 700;
    color: #f6d84a;
    text-transform: lowercase;
  }

  .logo-nike {
    height: 28px;
    display: block;
  }

 
  .menu {
    display: flex;
    gap: 3rem;
    transition: 0.3s ease;

    a {
      color: #f9e9d9;
      text-decoration: none;
      font-weight: 500;
      font-size: 0.95rem;

      &:hover {
        text-decoration: underline;
      }
    }
  }


  .hamburger {
    display: none;
    cursor: pointer;
    flex-direction: column;
    gap: 5px;

    span {
      width: 26px;
      height: 3px;
      background: #f6d84a;
      border-radius: 3px;
      transition: 0.3s ease;
    }
  }
}


.hero-name {
  background: #d6e02a;
  color: #0d1628;
  text-align: center;
  font-weight: 800;
  font-size: clamp(3.5rem, 14vw, 8rem);
  line-height: 1.1;
  padding: 4rem 1rem;
}


@media (max-width: 992px) {
  .top-nav {
    padding: 1.2rem 2rem;

    .menu {
      display: none; /* Hide menu by default */

      &.open {
        display: flex; 
        flex-direction: column;
        text-align: center;
        background: #b2391f;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        padding: 1.5rem 0;
        gap: 1.5rem;
        z-index: 10;
      }
    }

    .hamburger {
      display: flex; 
    }
  }

  .hero-name {
    padding: 3rem 1.2rem;
  }
}


@media (max-width: 480px) {
  .top-nav {
    padding: 1rem 1.2rem;

    .logo-be {
      font-size: 1.6rem;
    }

    .logo-nike {
      height: 22px;
    }
  }
}
</style>
