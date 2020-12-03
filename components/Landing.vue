<template>
  <div class="hero-container">
    <img class="hero--image" src="landing.svg" />
    <div class="hero--text">
      <h1 class="hero--heading">Project Karobaar</h1>
      <h3 class="hero--subheading">
        PROJECT KAROBAAR is an SaaS for local Businesses that provides various
        solutions based on their needs.
      </h3>
    </div>
    <div class="hero-connect">
      <h5 class="hero--caption">Connect us Here!</h5>
      <div class="link-icons">
        <a href="https://github.com/ProjectKarobaar" target="_blank">
          <vs-button size="xl" color="transparent" circle icon floating>
            <img src="icons/github.svg" class="social-icon" />
          </vs-button>
        </a>
        <a
          href="https://docs.google.com/presentation/d/1_zXKY17Gap06smqytPBjeBAperFBCrWwoCAJSQqg4I8/edit#slide=id.p"
          target="_blank"
        >
          <vs-button size="xl" color="transparent" circle icon floating>
            <img src="icons/file.svg" class="social-icon" />
          </vs-button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
}
</script>

<style lang="scss" scoped>
.hero-container {
  display: grid;
  place-items: center;
  gap: 3em;
}
.hero--image {
  max-width: 20em;
  margin: 0 auto;
}
.hero--text {
  text-align: center;
  padding: 0 1.5rem;
}
.hero--heading {
  font-weight: 700;
  font-size: 2.2rem;
  letter-spacing: 1px;
}
.hero--subheading {
  font-weight: 300;
  color: #616161;
  font-size: 1rem;
  text-align: center;
}
.social-icon {
  width: 72px;
  height: 72px;
}
.hero--connect {
  text-align: center;
}
.hero--caption {
  display: block;
  text-align: center;
}

.link-icons {
  display: flex;
  gap: 16px;
  padding: 18px 0;
}
@media only screen and (min-width: 600px) {
  .hero--image {
    max-width: 22em;
  }
  .hero--heading {
    font-size: 4.5rem;
  }
  .hero--subheading {
    font-size: 1.2rem;
  }
}
</style>
