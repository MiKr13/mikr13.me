<template>
  <section class="qualification section" id="qualification">
    <h2 class="section__title">Qualification</h2>
    <span class="section__subtitle">My personal qualification journey</span>

    <div class="qualification__container container">
      <div class="qualification__tabs">
        <div
          class="qualification__button button--flex"
          :class="{
            qualification__active: qualificationActive === 'education',
          }"
          @click="toggleQualification('education')"
        >
          <i class="uil uil-graduation-cap qualification__icon"></i>
          Education
        </div>

        <div
          class="qualification__button button--flex"
          :class="{
            qualification__active: qualificationActive === 'work',
          }"
          @click="toggleQualification('work')"
        >
          <i class="uil uil-briefcase-alt qualification__icon"></i>
          Work
        </div>
      </div>

      <div class="qualification__sections">
        <!-- ======== Qualification Content 1 ============= -->
        <div
          class="qualification__content"
          :class="{
            qualification__active: qualificationActive === 'education',
          }"
          id="education"
        >
          <!-- ======== Qualification 1 ============= -->
          <div class="qualification__data">
            <div>
              <h3 class="qualification__title">Computer Engineer</h3>
              <span class="qualification__subtitle">Peru - University</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2009 - 2014
              </div>
            </div>

            <div>
              <span class="qualification__rounder"></span>
              <span class="qualification__line"></span>
            </div>
          </div>
          <!-- ======== Qualification 2 ============= -->
          <div class="qualification__data">
            <div></div>
            <div>
              <span class="qualification__rounder"></span>
              <span class="qualification__line"></span>
            </div>

            <div>
              <h3 class="qualification__title">Post Graduate</h3>
              <span class="qualification__subtitle">Peru - University</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2014 - 2015
              </div>
            </div>
          </div>
          <!-- ======== Qualification 3 ============= -->
          <div class="qualification__data">
            <div>
              <h3 class="qualification__title">Computer Scientist</h3>
              <span class="qualification__subtitle">Peru - University</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2015 - 2018
              </div>
            </div>

            <div>
              <span class="qualification__rounder"></span>
              <!-- <span class="qualification__line"></span> -->
            </div>
          </div>
        </div>

        <!-- ======== Qualification Content 2 ============= -->
        <div
          class="qualification__content"
          :class="{
            qualification__active: qualificationActive === 'work',
          }"
          id="work"
        >
          <!-- ======== Qualification 1 ============= -->
          <div class="qualification__data">
            <div>
              <h3 class="qualification__title">Software Engineer</h3>
              <span class="qualification__subtitle">Microsoft - Peru</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2016 - 2018
              </div>
            </div>

            <div>
              <span class="qualification__rounder"></span>
              <span class="qualification__line"></span>
            </div>
          </div>
          <!-- ======== Qualification 2 ============= -->
          <div class="qualification__data">
            <div></div>
            <div>
              <span class="qualification__rounder"></span>
              <span class="qualification__line"></span>
            </div>

            <div>
              <h3 class="qualification__title">Software Engineer</h3>
              <span class="qualification__subtitle">Apple - Spain</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2016 - 2019
              </div>
            </div>
          </div>
          <!-- ======== Qualification 3 ============= -->
          <div class="qualification__data">
            <div>
              <h3 class="qualification__title">Software Researcher</h3>
              <span class="qualification__subtitle">MongoDB - Spain</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2019 - 2021
              </div>
            </div>

            <div>
              <span class="qualification__rounder"></span>
              <span class="qualification__line"></span>
            </div>
          </div>
          <!-- ======== Qualification 4 ============= -->
          <div class="qualification__data">
            <div></div>
            <div>
              <span class="qualification__rounder"></span>
              <!-- <span class="qualification__line"></span> -->
            </div>

            <div>
              <h3 class="qualification__title">CTO</h3>
              <span class="qualification__subtitle">Pepsi - Spain</span>
              <div class="qualification__calendar">
                <i class="uil uil-calendar-alt"></i>
                2021 - 2025
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from "vue"
export default {
  setup() {
    let qualificationActive = ref("education")

    function toggleQualification(value) {
      qualificationActive.value = value
    }

    return {
      qualificationActive,
      toggleQualification,
    }
  },
}
</script>

<style>
.qualification__tabs {
  display: flex;
  justify-content: space-evenly;
  margin-bottom: var(--mb-2);
}

.qualification__button {
  font-size: var(--h3-font-size);
  font-weight: var(--font-medium);
  cursor: pointer;
}

.qualification__button:hover {
  color: var(--first-color);
}

.qualification__icon {
  font-size: 1.8rem;
  margin-right: var(--mb-0-25);
}

.qualification__data {
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}

.qualification__title {
  font-size: var(--normal-font-size);
  font-weight: var(--font-medium);
}

.qualification__subtitle {
  display: inline-block;
  font-size: var(--small-font-size);
  margin-bottom: var(--mb-1);
}

.qualification__calendar {
  font-size: var(--smaller-font-size);
  color: var(--text-color-light);
}

.qualification__rounder {
  display: inline-block;
  width: 13px;
  height: 13px;
  background-color: var(--first-color);
  border-radius: 50%;
  -webkit-border-radius: 50%;
  -moz-border-radius: 50%;
  -ms-border-radius: 50%;
  -o-border-radius: 50%;
}

.qualification__line {
  display: block;
  width: 1px;
  height: 100%;
  background-color: var(--first-color);
  transform: translate(6px, -7px);
  -webkit-transform: translate(6px, -7px);
  -moz-transform: translate(6px, -7px);
  -ms-transform: translate(6px, -7px);
  -o-transform: translate(6px, -7px);
}

.qualification__content {
  display: none;
}

.qualification__active {
  display: block;
}

.qualification__button.qualification__active {
  color: var(--first-color);
}
</style>
