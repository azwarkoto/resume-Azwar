<template>
  <div
    id="portofolio"
    data-aos="fade-up"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out"
  >
    <div class="p-card">
      <h5 class="mb-3">Portfolio</h5>

      <div class="row mb-2">
        <div class="col-12">
          <div class="detail-img">
            <img
              :src="require('@/assets/img/portofolio/' + detail.img)"
              class="w-100"
              style="border-radius: 15px"
            />
          </div>
          <div class="p-title">{{ detail.title }}</div>
          <div class="p-label">Description</div>
          <div class="p-description">
            {{ detail.desc }}
          </div>

          <div class="p-tech justify-content-between">
            <div class="text">Technology</div>
            <div class="p-icon">
              <div class="float-end">
                <div class="d-flex">
                  <i class="circle" v-for="i in detail.tech" :key="i">
                    <img :src="require('@/assets/img/icon/' + i)" />
                  </i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <Splide
        :options="{
          // autoplay: true,
          perPage: 2,
          width: '100%',
          interval: 4000,
          gap: 10,
          // type: 'loop',
          arrows: false,
          pagination: false,
          padding: { left: 0, right: 40 },
        }"
      >
        <SplideSlide
          class="position-relative overflow-hidden shadow-sm"
          v-for="i in list"
          :key="i"
        >
          <div class="card-list" @click="chekDetail(i)">
            <div class="img-sum position-relative overflow-hidden">
              <img
                :src="require('@/assets/img/portofolio/' + i.img)"
                class="w-100"
              />
              <div class="title-sum text-center">
                <p class="my-0">{{ i.title }}</p>
              </div>
            </div>
          </div>
        </SplideSlide>
      </Splide>
    </div>
  </div>
</template>

<script>
export default {
  name: "portofolioComp",
  components: {},
  data() {
    return {
      detail: {
        title: "Internal Operation System",
        img: "portofolio.webp",
        desc: "Sartifikat.",
        tech: [
          "back-end/codeigniter.svg",
          "back-end/mysql-4.svg",
          "front-end/html-1.svg",
          "front-end/css-3.svg",
          "front-end/jquery.svg",
          "front-end/bootstrap-5-1.svg",
        ],
      },
      list: [
        {
          title: "Sartifikat Java Script",
          img: "javaScript.webp",
          desc: "Sartifikat Java Script.",
          tech: [
            "back-end/codeigniter.svg",
            "front-end/css-3.svg",
            "front-end/html-1.svg",
            "back-end/mysql-4.svg",
            "front-end/bootstrap-5-1.svg",
            "front-end/jquery.svg",
          ],
        },
        {
          title: "Sartifikat Udemy ",
          img: "udemy Learn-Flutter-3.0-Firebase---Develop-iOS-Android-Food-Delivery-Food.webp",
          desc: "Sartifikat Learn-Flutter-3.0-Firebase---Develop-iOS-Android-Food-Delivery-Food",
          tech: [
            "back-end/codeigniter.svg",
            "front-end/html-1.svg",
            "back-end/mysql-4.svg",
            "front-end/jquery.svg",
            "front-end/css-3.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },
        {
          title: "Sartifikat Udemy",
          img: "udemy Flutter-Firebase-by-Google---Build-iOS-Android-Taxi-Ride.webp",
          desc: "Sartifikat lutter-Firebase-by-Google---Build-iOS-Android-Taxi-Ride.",
          tech: [
            "back-end/codeigniter.svg",
            "back-end/mysql-4.svg",
            "front-end/css-3.svg",
            "front-end/html-1.svg",
            "front-end/bootstrap-5-1.svg",
            "front-end/jquery.svg",
          ],
        },
        {
          title: "Sartifikat Php",
          img: "php.webp",
          desc: "Sartiifkat Php.",
          tech: [
            "back-end/laravel-2.svg",
            "back-end/mysql-4.svg",
            "front-end/html-1.svg",
            "front-end/jquery.svg",
            "front-end/css-3.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },
        {
          title: "Sartifikat Html ",
          img: "html.webp",
          desc: "Sartifikat Html.",
          tech: [
            "back-end/laravel-2.svg",
            "back-end/mysql-4.svg",
            "front-end/vue-9.svg",
            "front-end/html-1.svg",
            "front-end/css-3.svg",
            "front-end/jquery.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },

         {
          title: "Sartifikat Java",
          img: "java.webp",
          desc: "Sartiifkat Php.",
          tech: [
            "back-end/laravel-2.svg",
            "back-end/mysql-4.svg",
            "front-end/html-1.svg",
            "front-end/jquery.svg",
            "front-end/css-3.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },

         {
          title: "Sartifikat Jquery",
          img: "jquery.webp",
          desc: "Sartiifkat Php.",
          tech: [
            "back-end/laravel-2.svg",
            "back-end/mysql-4.svg",
            "front-end/html-1.svg",
            "front-end/jquery.svg",
            "front-end/css-3.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },

          {
          title: "Sartifikat CSS",
          img: "css.webp",
          desc: "Sartiifkat Php.",
          tech: [
            "back-end/laravel-2.svg",
            "back-end/mysql-4.svg",
            "front-end/html-1.svg",
            "front-end/jquery.svg",
            "front-end/css-3.svg",
            "front-end/bootstrap-5-1.svg",
          ],
        },
        
      ],
    };
  },
  methods: {
    chekDetail(i) {
      this.detail = i;
    },
  },
};
</script>

<style lang="scss">
#portofolio {
  margin-top: -20px;
  background: var(--color-6);
  padding: 40px 20px 50px 20px;
  border-radius: 30px 30px 0 0;
}

.p-card {
  position: relative;
  border-radius: 10px !important;
}

.p-slide img {
  position: relative;
  z-index: 0;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  object-fit: cover;
  object-position: center;
  transition: transform 0.3s;
}

.p-slide img:hover {
  transform: scale(1.1);
}

.ription {
  position: absolute;
  bottom: -100%;
  left: 0;
  width: 100%;
  height: 70%;
  background: var(--color-4);
  color: var(--text-color-4);
  margin: auto;
  z-index: 9;
  padding: 20px;
  font-size: 1em;
  border-radius: 0 0 10px 10px;
  text-align: center;
  display: flex;
  align-items: center;
  transition: all 0.3s ease-in-out;
}

.card-pt:hover .ription {
  bottom: 0;
}

.detail-img {
  position: relative;
  overflow: hidden;
  height: 250px;
  border-radius: 15px;
}

.detail-img img {
  object-fit: cover;
  object-position: top;
  height: 100%;
  transition: all 0.3s ease-in-out;
}

.detail-img:hover img {
  transform: scale(1.1);
}

.p-title {
  font-size: 1.1em;
  font-weight: 600;
  margin: 15px 0 10px 0;
}

.p-label {
  font-size: 1em;
  font-weight: 500;
  margin-bottom: 5px;
}

.p-description {
  font-size: 0.9em;
  margin-bottom: 10px;
}

.p-tech {
  display: flex;
  align-items: center;
  background: var(--color-2);
  border-radius: 15px;
  margin-top: 15px;
}

.p-tech .text {
  padding-left: 10px;
  font-size: 0.8em;
}

.p-icon {
  background: var(--color-1);
  padding: 5px 10px;
  border-radius: 15px;
  transition: all 0.3s ease-in-out;
}

.circle {
  width: 30px;
  height: 30px;
  background: #fff;
  border-radius: 30px;
  margin: 0 2px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.circle img {
  width: 60%;
}

.card-list {
  background: var(--color-5);
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
}

.img-sum {
  height: 80px;
}

.img-sum img {
  height: 100%;
  object-fit: cover;
  object-position: center;
  // border-radius: 10px;
  // animation: slide 3s ease-in-out alternate infinite;
}

.title-sum {
  position: absolute;
  background: var(--color-1);
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0.9;
  transition: all 0.3s;
}

.title-sum p {
  font-size: 0.8em !important;
  padding: 10px;
  line-height: 15px !important;
  color: var(--text-color-1);
}

.img-sum:hover .title-sum {
  left: 0;
}
</style>