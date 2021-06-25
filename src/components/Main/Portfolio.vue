<template>
  <section class="portfolio section" id="portfolio">
    <h2 class="section__title">Portfolio</h2>
    <span class="section__subtitle"
      >My projects & Open Source contributions</span
    >

    <div class="portfolio__container container">
      <swiper
        :cssMode="true"
        :slides-per-view="1"
        :loop="true"
        :mousewheel="true"
        :keyboard="true"
        :pagination="{ clickable: true }"
        :navigation="true"
      >
        <!-- ======== Portfolio 1 ============= -->
        <swiper-slide
          ><div class="portfolio__content grid">
            <img
              src="../../assets/images/portfolio1.jpg"
              alt=""
              class="portfolio__img"
            />

            <div class="portfolio__data">
              <h3 class="portfolio__title">Modern Website</h3>
              <p class="portfolio__description">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut
                dolorem dolore minus quod debitis ducimus nam neque quisquam
                repudiandae a. Facilis harum consequatur architecto sunt minus
                totam delectus sit officiis?
              </p>
              <a
                href="#"
                class="button button--flex button--small portfolio__button"
              >
                Demo
                <i class="uil uil-arrow-right button__icon"></i>
              </a>
            </div></div
        ></swiper-slide>
        <!-- ======== Portfolio 2 ============= -->
        <swiper-slide
          ><div class="portfolio__content grid">
            <img
              src="../../assets/images/portfolio2.jpg"
              alt=""
              class="portfolio__img"
            />

            <div class="portfolio__data">
              <h3 class="portfolio__title">Brand Design</h3>
              <p class="portfolio__description">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut
                dolorem dolore minus quod debitis ducimus nam neque quisquam
                repudiandae a. Facilis harum consequatur architecto sunt minus
                totam delectus sit officiis?
              </p>
              <a
                href="#"
                class="button button--flex button--small portfolio__button"
              >
                Demo
                <i class="uil uil-arrow-right button__icon"></i>
              </a>
            </div></div
        ></swiper-slide>
        <!-- ======== Portfolio 3 ============= -->
        <swiper-slide
          ><div class="portfolio__content grid">
            <img
              src="../../assets/images/portfolio3.jpg"
              alt=""
              class="portfolio__img"
            />

            <div class="portfolio__data">
              <h3 class="portfolio__title">Crazy Collector</h3>
              <p class="portfolio__description">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut
                dolorem dolore minus quod debitis ducimus nam neque quisquam
                repudiandae a. Facilis harum consequatur architecto sunt minus
                totam delectus sit officiis?
              </p>
              <a
                href="#"
                class="button button--flex button--small portfolio__button"
              >
                Demo
                <i class="uil uil-arrow-right button__icon"></i>
              </a>
            </div></div
        ></swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
import SwiperCore, {
  Navigation,
  Pagination,
  Mousewheel,
  Keyboard,
} from "swiper/core"
import { Swiper, SwiperSlide } from "swiper/vue"

import "swiper/swiper-bundle.min.css"

SwiperCore.use([Navigation, Pagination, Mousewheel, Keyboard])

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
}
</script>

<style>
.portfolio__container {
  overflow: initial;
}

.portfolio__content {
  padding: 1rem 1.5rem;
}

.portfolio__img {
  width: 265px;
  border-radius: 0.5rem;
  -webkit-border-radius: 0.5rem;
  -moz-border-radius: 0.5rem;
  -ms-border-radius: 0.5rem;
  -o-border-radius: 0.5rem;
  justify-self: center;
}

.portfolio__title {
  font-size: var(--h3-font-size);
  margin-bottom: var(--mb-0-5);
}

.portfolio__description {
  margin-bottom: var(--mb-0-75);
}

.portfolio__button:hover .button__icon {
  transform: translateX(0.25rem);
  -webkit-transform: translateX(0.25rem);
  -moz-transform: translateX(0.25rem);
  -ms-transform: translateX(0.25rem);
  -o-transform: translateX(0.25rem);
}

.swiper-button-prev::after,
.swiper-button-next::after {
  font-size: 1.25rem;
  color: var(--first-color);
  font-weight: var(--font-semi-bold);
}

.swiper-button-prev {
  left: -0.5rem;
}

.swiper-button-next {
  right: -0.5rem;
}

.swiper-container-horizontal > .swiper-pagination-bullets {
  bottom: -0.25rem;
}

.swiper-pagination-bullet-active {
  background: var(--first-color);
}

.swiper-button-prev,
.swiper-button-next,
.swiper-pagination-bullet {
  outline: none;
}
</style>
