<template>
  <div
    id="education"
    data-aos="fade-up"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out"
  >
    <div class="title">Education</div>
    <Splide
      :options="{
        perPage: 1,
        width: '100%',
        gap: 10,
        arrows: false,
        pagination: false,
        padding: { left: 0, right: 130 },
      }"
    >
      <SplideSlide>
        <div class="edu-card">
          <div class="school">
            <h4>SMP Al -  WASHLIYAH  </h4>
            <h5>JAKARTA</h5>
          </div>
          <div class="year">2009-2012</div>
          <div class="edu-img">
            <i class="fa-solid fa-graduation-cap"></i>
          </div>
        </div>
      </SplideSlide>
      <SplideSlide>
        <div class="edu-card">
          <div class="school">
            <h4>Smk Dinamika </h4>
            <h5>Jakarta</h5>
          </div>
          <div class="year">2012-2015</div>
          <div class="edu-img">
            <i class="fa-solid fa-graduation-cap"></i>
          </div>
        </div>
      </SplideSlide>
      <SplideSlide>
        <div class="edu-card">
          <div class="school">
            <h4>Universitas BSI </h4>
            <h5>Surakarta</h5>
          </div>
          <div class="year">2015-2018</div>
          <div class="edu-img">
            <i class="fa-solid fa-graduation-cap"></i>
          </div>
        </div>
      </SplideSlide>
    </Splide>
  </div>
</template>

<script>
export default {
  name: "eduComp",
};
</script>

<style lang="scss">
#education {
  position: relative;
  z-index: 1;
  padding: 20px;
  border-radius: 0 0 40px 40px;
  background: var(--color-6);
}

.edu-content {
  position: relative;
  width: 100%;
  padding-bottom: 20px;
  overflow: auto;
  display: flex;
}

.edu-card {
  transition: all 0.4s;
  position: relative;
  background: var(--color-1);
  // background-image: linear-gradient(-45deg, var(--secondary), var(--third));
  color: var(--text-color-1);
  box-shadow: var(--color-2);
  min-width: 60%;
  border-radius: 20px;
  padding: 10px 20px;
  z-index: 1;
  overflow: hidden;
}

.edu-card::before {
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url("../assets/img/pattern.webp");
  background-size: 50%;
  opacity: 0.1;
}

.school {
  min-height: 50px;
}

.school h4 {
  font-size: 1.2em;
  margin-bottom: 0;
}

.school h5 {
  font-size: 1em;
}

.year {
  background: var(--color-2);
  display: inline;
  padding: 5px 10px;
  border-radius: 20px;
  color: var(--text-color-2);
  font-size: 0.7em;
}

.edu-img {
  position: absolute;
  right: -40px;
  bottom: -40px;
  font-size: 7em;
  transform: rotate(-40deg);
  opacity: 0.1;
  color: var(--text-color-1);
  transition: all 0.3s ease-in-out;
  z-index: -1;
}

.edu-card:hover .edu-img,
.edu-img:hover {
  transform: rotate(-20deg);
}
</style>