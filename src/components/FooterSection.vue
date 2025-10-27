<template>
  <header class="top-nav">
    <div class="nav-left">
      <span class="logo-be">be</span>
    </div>

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

    <div class="nav-right">
      <img class="logo-nike" src="@/assets/images/nike-logo.svg" alt="nike logo" />
    </div>

    
  </header>

  <section class="hero-name">
    Brooke Eaaaleeve
  </section>
</template>

<style scoped lang="scss">
.top-nav {
  background: linear-gradient(90deg, #b2391f, #e06a28);
  padding: 1.2rem 3rem;
  display: flex;
  align-items: center;
  justify-content: space-between;

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
}


.hero-name {
  background: #d6e02a;
  color: #0d1628;      
  text-align: center;
  font-weight: 800;
  font-size: clamp(8rem, 8vw, 7rem);
  line-height: 1.1;
  padding: 4rem 1rem;
}
</style>