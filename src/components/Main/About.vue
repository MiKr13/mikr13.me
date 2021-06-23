<template>
  <section class="about section" id="about">
    <h2 class="section__title">About Me</h2>
    <span class="section__subtitle">My introduction</span>

    <div class="about__container container grid">
      <img src="../../assets/images/about.jpg" alt="" class="about__img" />

      <div class="about__data">
        <p class="about__description">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor iusto
          repudiandae totam? Illo cumque repudiandae nobis nemo voluptates eaque
          deserunt laboriosam modi rem temporibus qui reprehenderit commodi,
          ullam impedit perspiciatis.
        </p>

        <div class="about__info">
          <div>
            <span class="about__info-title">08+</span>
            <span class="about__info-name"
              >Year <br />
              experience</span
            >
          </div>
          <div>
            <span class="about__info-title">20+</span>
            <span class="about__info-name"
              >Completed <br />
              projects</span
            >
          </div>
          <div>
            <span class="about__info-title">04+</span>
            <span class="about__info-name"
              >Companies <br />
              worked</span
            >
          </div>
        </div>

        <div class="about__buttons">
          <a
            download=""
            href="../../assets/pdf/Mihir-Kumar-Resume.pdf"
            class="button button--flex"
          >
            Download Resume <i class="uil uil-download-alt button__icon"></i>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style>
.about__img {
  width: 200px;
  border-radius: 0.5rem;
  -webkit-border-radius: 0.5rem;
  -moz-border-radius: 0.5rem;
  -ms-border-radius: 0.5rem;
  -o-border-radius: 0.5rem;
  justify-self: center;
  align-self: center;
}

.about__description {
  text-align: center;
  margin-bottom: var(--mb-2-5);
}

.about__info {
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2-5);
}

.about__info-title {
  font-size: var(--h2-font-size);
  font-weight: var(--font-semi-bold);
  color: var(--title-color);
}

.about__info-name {
  font-size: var(--smaller-font-size);
}

.about__info-title,
.about__info-name {
  display: block;
  text-align: center;
}

.about__buttons {
  display: flex;
  justify-content: center;
}
</style>
