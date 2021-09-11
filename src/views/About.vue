<template>
  <div class="about">
    <div class="row header-image relative">
      <img src="@/assets/section/about-main.jpg" alt="camera" />
    </div>
    <div class="width-lg">
      <div class="absolute-center">
        <div class="about-heading">
          <h1 class="q-my-sm">About Us</h1>
        </div>
      </div>
      <div class="row text-center">
        <h6 class="q-my-sm">
          Digital System was formed in Canada, in the year 2010. Since we have
          started our intention is to supply the best solutions to our clients.
          We are a team designed to operate as one. We set the values, focused
          on client impact. We always take a consistent approach to enhance the
          skills of our people. Digital System is not only providing the
          ‘solutions’ but also offers great opportunities for our team members
          by working in a competitive era of technology for learning something
          new.
        </h6>
      </div>
      <div class="row">
        <div class="col col-xs-12 col-sm-6 q-my-auto">
          <h6 class="q-my-sm">
            Being a trust-able name in the town we have the impressive portfolio
            of installing security solutions, and offering other services
            including Home Cloud Solutions, Advanced protection Solutions etc.
            We have a long-term business relationship with the several companies
            being a complete package for our existing and future clients.
          </h6>
        </div>
        <div class="col col-xs-12 col-sm-6 q-pa-md">
          <img class="cctv-img" src="@/assets/section/cctv.jpeg" />
        </div>
      </div>
      <div class="row">
        <div class="col col-xs-12 col-sm-6">
          <img
            class="cctv-img q-pa-md"
            src="@/assets/section/experience.jpeg"
          />
        </div>
        <div class="col col-xs-12 col-sm-6 q-my-auto">
          <h6 class="q-my-sm">
            We have expert teams of security solutions, each team member has
            minimum five years of experience in the relevant industry. They can
            help you to transform your business to the next levels by putting
            their creative skills. At Digital System, we understand our
            responsibilities and provide the best quality in each area of our
            expertise and guide our clients to promote their business online
            with the right strategy.
          </h6>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.about {
  .about-heading {
    background-color: white;
    opacity: 0.9;
    color: #027f9a;
    padding: 25px;
  }
  .absolute-center {
    top: 62% !important;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .header-image {
    background-color: black;
    img {
      width: 100%;
      height: 500px;
      object-fit: cover;
      opacity: 0.4;
    }
  }
  .cctv-img {
    object-fit: cover;
    max-width: 600px;
    width: 100%;
    height: 300px;
  }
}
</style>
