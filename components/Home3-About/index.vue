<template>
  <section class="about-us section-padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-5 valign md-mb50">
          <div class="mb-50">
            <h6 class="fw-100 text-u ls10 main-color mb-10">About Us</h6>
            <h3 class="fw-600 text-u ls1 mb-30">Our Comapny</h3>
            <p>
              An Architectural Practice Established In 2015, Formerly Trading As
              Alpine Designs. Based In Malawi, Lilongwe We Are Involved In A
              Wide Range Of Projects All Sizes And Types. We Are Committed To
              Designing And Delivering Meaningful And Valuable Architecture
              Projects Indebted To Their Context And People.
            </p>
            <NuxtLink to="#0" class="btn-curve btn-bord btn-lit mt-30">
              <span>Read More</span>
            </NuxtLink>
          </div>
        </div>
        <div class="col-lg-7 img">
          <img src="/img/feat.jpg" alt="" />
          <div class="stauts">
            <div class="item" v-for="(stat, idx) in aboutData" :key="idx">
              <h4>
                {{ stat.number }}<span>{{ stat.operator }}</span> +
              </h4>
              <h6>{{ stat.title }}</h6>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Home3AboutData from "../../data/home3-about.json";

export default {
  name: "Home3-About",
  data() {
    return {
      aboutData: Home3AboutData,
    };
  },
};
</script>
