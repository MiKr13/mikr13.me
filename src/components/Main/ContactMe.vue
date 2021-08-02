<template>
  <section class="contact section" id="contac">
    <h2 class="section__title">Contact Me</h2>
    <span class="section__subtitle">Get in touch</span>

    <div class="contact__container container grid">
      <div>
        <div class="contact__information">
          <i class="uil uil-phone contact__icon"></i>

          <div>
            <h3 class="contact__title">Call Me</h3>
            <span class="contact__subtitle">999-777-666</span>
          </div>
        </div>
        <div class="contact__information">
          <i class="uil uil-envelope contact__icon"></i>

          <div>
            <h3 class="contact__title">Email</h3>
            <span class="contact__subtitle"
              ><a href="mailto:mihirpandey.13@gmail.com"
                >mihirpandey.13@gmail.com</a
              ></span
            >
          </div>
        </div>
        <div class="contact__information">
          <i class="uil uil-linkedin contact__icon"></i>

          <div>
            <h3 class="contact__title">LinkedIn</h3>
            <span class="contact__subtitle"
              ><a href="https://linkedin.com/in/mikr13">in/mikr13</a></span
            >
          </div>
        </div>
        <div class="contact__information">
          <i class="uil uil-github contact__icon"></i>

          <div>
            <h3 class="contact__title">GitHub</h3>
            <span class="contact__subtitle"
              ><a href="https://github.com/mikr13">@mikr13</a></span
            >
          </div>
        </div>
      </div>

      <form action="" class="contact__form grid">
        <div class="contact__inputs grid">
          <div class="contact__content">
            <label for="name" class="contact__label">Name</label>
            <input type="text" id="name" name="name" class="contact__input" />
          </div>
          <div class="contact__content">
            <label for="email" class="contact__label">Email</label>
            <input type="text" id="email" name="email" class="contact__input" />
          </div>
          <div class="contact__content">
            <label for="subject" class="contact__label">Subject</label>
            <input
              type="text"
              id="subject"
              name="subject"
              class="contact__input"
            />
          </div>
          <div class="contact__content">
            <label for="message" class="contact__label">Message</label>
            <textarea
              type="text"
              id="message"
              name="message"
              cols="0"
              rows="7"
              class="contact__input"
            ></textarea>
          </div>

          <div>
            <a href="#" class="button button--flex">
              Send Message
              <i class="uil uil-message button__icon"></i>
            </a>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.contact__container {
  row-gap: 3rem;
}

.contact__information {
  display: flex;
  margin-bottom: var(--mb-2);
}

.contact__icon {
  font-size: 2rem;
  color: var(--first-color);
  margin-right: var(--mb-0-75);
}

.contact__title {
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
}

.contact__subtitle {
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.contact__content {
  background-color: var(--input-color);
  border-radius: 0.5rem;
  padding: 0.75rem 1rem 0.25rem;
}

.contact__label {
  font-size: var(--smaller-font-size);
  color: var(--title-color);
}

.contact__input {
  width: 100%;
  background-color: var(--input-color);
  color: var(--text-color);
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  border: none;
  outline: none;
  padding: 0.25rem 0.5rem 0.5rem 0;
}
</style>
