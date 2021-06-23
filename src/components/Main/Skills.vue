<template>
  <section class="skills section" id="skills">
    <h2 class="section__title">Skills</h2>
    <span class="section__subtitle">My technical level</span>

    <div class="skills__container container grid">
      <div>
        <!--=========== Skill 1 ================-->
        <div class="skills__content skills__open">
          <div class="skills__header" @click="toggleSkill($event)">
            <i class="uil uil-brackets-curly skills__icon"></i>

            <div>
              <h1 class="skills_title">Frontend developer</h1>
              <span class="skills__subtitle">More than 4 years</span>
            </div>

            <i class="uil uil-angle-down skills__arrow"></i>
          </div>

          <div class="skills__list grid">
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  HTML
                </h3>
                <span class="skills__number">90%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__html"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  CSS
                </h3>
                <span class="skills__number">80%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__css"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  JS
                </h3>
                <span class="skills__number">80%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__js"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Vue
                </h3>
                <span class="skills__number">85%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__vue"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  React
                </h3>
                <span class="skills__number">85%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__react"></span>
              </div>
            </div>
          </div>
        </div>
        <!--=========== Skill 2 ================-->
        <div class="skills__content skills__close">
          <div class="skills__header" @click="toggleSkill($event)">
            <i class="uil uil-server-network skills__icon"></i>

            <div>
              <h1 class="skills_title">Backend developer</h1>
              <span class="skills__subtitle">More than 5 years</span>
            </div>

            <i class="uil uil-angle-down skills__arrow"></i>
          </div>

          <div class="skills__list grid">
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  NodeJS
                </h3>
                <span class="skills__number">90%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__nodejs"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Go
                </h3>
                <span class="skills__number">50%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__go"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Firebase
                </h3>
                <span class="skills__number">70%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__firebase"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Python
                </h3>
                <span class="skills__number">65%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__python"></span>
              </div>
            </div>
          </div>
        </div>
        <!--=========== Skill 3 ================-->
        <div class="skills__content skills__close">
          <div class="skills__header" @click="toggleSkill($event)">
            <i class="uil uil-swatchbook skills__icon"></i>

            <div>
              <h1 class="skills_title">Designer</h1>
              <span class="skills__subtitle">More than 5 years</span>
            </div>

            <i class="uil uil-angle-down skills__arrow"></i>
          </div>

          <div class="skills__list grid">
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Figma
                </h3>
                <span class="skills__number">50%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__figma"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Sketch
                </h3>
                <span class="skills__number">70%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__sketch"></span>
              </div>
            </div>
            <div class="skills__data">
              <div class="skills__title">
                <h3 class="skills__name">
                  Storybook
                </h3>
                <span class="skills__number">70%</span>
              </div>
              <div class="skills__bar">
                <span class="skills__percentage skills__storybook"></span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  setup() {
    function toggleSkill(event) {
      event.stopPropagation()
      let skillsContent = document.getElementsByClassName("skills__content")
      let parent = event.target
      while (!parent.classList.contains("skills__content")) {
        parent = parent.parentNode
      }

      for (let skill of skillsContent) {
        skill.className = "skills__content skills__close"
      }

      if (parent.classList.value === "skills__content skills__close") {
        parent.className = "skills__content skills__open"
      }
    }

    return {
      toggleSkill,
    }
  },
}
</script>

<style>
.skills__container {
  row-gap: 0;
}

.skills__header {
  display: flex;
  align-items: center;
  margin-bottom: var(--mb-2-5);
  cursor: pointer;
}

.skills__icon,
.skills__arrow {
  font-size: 2rem;
  color: var(--first-color);
}

.skills__icon {
  margin-right: var(--mb-0-75);
}

.skills__title {
  font-size: var(--h3-font-size);
}

.skills__subtitle {
  font-size: var(--small-font-size);
  color: var(--text-color-light);
}

.skills__arrow {
  margin-left: auto;
  transition: 0.4s;
  -webkit-transition: 0.4s;
  -moz-transition: 0.4s;
  -ms-transition: 0.4s;
  -o-transition: 0.4s;
}

.skills__list {
  row-gap: 1.5rem;
  padding-left: 2.7rem;
}

.skills__title {
  display: flex;
  justify-content: space-between;
  margin-bottom: var(--mb-0-5);
}

.skills__name {
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.skills__bar,
.skills__percentage {
  height: 5px;
  border-radius: 0.25rem;
  -webkit-border-radius: 0.25rem;
  -moz-border-radius: 0.25rem;
  -ms-border-radius: 0.25rem;
  -o-border-radius: 0.25rem;
}

.skills__bar {
  background-color: var(--first-color-lighter);
}

.skills__percentage {
  display: block;
  background-color: var(--first-color);
}

.skills__html {
  width: 90%;
}

.skills__css {
  width: 80%;
}

.skills__js {
  width: 80%;
}

.skills__vue {
  width: 85%;
}

.skills__react {
  width: 85%;
}

.skills__nodejs {
  width: 90%;
}

.skills__go {
  width: 50%;
}

.skills__firebase {
  width: 70%;
}

.skills__python {
  width: 65%;
}

.skills__figma {
  width: 50%;
}

.skills__sketch {
  width: 70%;
}

.skills__storybook {
  width: 70%;
}

.skills__close .skills__list {
  height: 0;
  overflow: hidden;
}

.skills__open .skills__list {
  height: max-content;
  margin-bottom: var(--mb-2-5);
}

.skills__open .skills__arrow {
  transform: rotate(-180deg);
  -webkit-transform: rotate(-180deg);
  -moz-transform: rotate(-180deg);
  -ms-transform: rotate(-180deg);
  -o-transform: rotate(-180deg);
}
</style>
