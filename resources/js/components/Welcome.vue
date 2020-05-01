<template>
  <div v-bind:class="{'no-scroll': modalVisible}">
    <div class="container">
      <!-- Section -->
      <div class="section">
        <h2 class="section__title">
          10 Best Photo Apps For Incredible iPhone Photography (2020
          Edition)
        </h2>
        <hr class="section__divider" />
        <p class="section__text">
          How do you capture more interesting travel photos with your
          iPhone? How do you avoid taking the same cliché vacation
          photos that everyone else takes? I recently interviewed
          Steffen Geldner - a talented iPhone photographer with a
          passion for travel. In this article, Steffen reveals 7 tips
          for shooting beautiful travel photos that will preserve the
          amazing memories of your trip. Read on to discover how to
          take better travel photos with your iPhone!
        </p>
        <div class="section__image-container">
          <div class="section__image-container__image"></div>
        </div>
        <h2 class="section__subtitle">
          1. Research Your Destination To Find The Best Photo
          Opportunities
        </h2>
        <p class="section__text">
          Before your trip, I recommend researching the destination to
          find the most interesting photo opportunities.
          <br />
          <br />I always research the location I'm traveling to. I do this
          extensively and obsessively!
          <br />
          <br />It's up to you how much research you do. But you should
          definitely spend a bit of time looking up some great places
          to take pictures.
          <br />
          <br />So. what kind of research can you do?
          <br />
          <br />First, you could search for photos that other people have
          taken at the locations you're planning to visit.
          <br />
          <br />Search on Instagram or Google to get an idea of the kinds of
          photos people take there.
        </p>
        <h2 class="section__subtitle">
          2. Capture Your Journey To Tell The Complete Story Of Your
          Travels
        </h2>
        <p class="section__text">
          Travel photography isn't just about photographing the
          destination.
          <br />
          <br />For a more complete photographic story, capture your journey
          to and from the location you're visiting.
          <br />
          <br />If you're traveling by plane. try to get a window seat where
          you have a view of the wing or propeller.
          <br />
          <br />And of course, you could capture a beautiful aerial view of
          clouds, mountains, or city lights as you're flying above.
          <br />
          <br />Your journey will often involve several different types of
          transport. And they all offer great photo opportunities.
          <br />
          <br />Whether you're traveling by car, taxi, bus, train, boat, or
          plane, try to capture some interesting photos.
        </p>
      </div>
      <!-- Section -->

      <!-- Sidebar -->
      <div class="sidebar">
        <button class="sidebar__gradient-button" @click="setModalVisible(true)">Send Me The Tips</button>
      </div>
      <!-- Sidebar -->
    </div>

    <!-- Modal -->
    <div v-if="modalVisible" class="modal">
      <div class="modal__card">
        <div class="modal__close-button" @click="setModalVisible(false)">×</div>
        <div class="modal__card__container">
          <small class="modal__card__container__progress-text">Step 1 of 2</small>
          <div
            class="modal__card__container__progress-bar modal__card__container__progress-bar--remaining"
          >
            <div
              class="modal__card__container__progress-bar modal__card__container__progress-bar--filled"
            ></div>
          </div>

          <h3 class="modal__card__container__text">
            Enter Your Email To Get
            <span>FREE</span>
            <br />iPhone Photography Email Tips:
          </h3>
          <form v-on:submit.prevent="onSubmit()" novalidate>
            <input
              class="modal__card__container__form-input"
              v-bind:class="{'modal__card__container__form-input--error': error}"
              type="email"
              name="email"
              id="email"
              v-bind:placeholder="placeholderText"
              required
              @change="(event) => onChange(event)"
            />
            <button class="modal__card__container__gradient-button" type="submit">Send Me The Tips »</button>
          </form>
        </div>
      </div>
    </div>
    <!-- Modal -->

    <!-- Modal Overlay -->
    <div v-if="modalVisible" class="overlay" />
    <!-- Modal Overlay -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      modalVisible: false,
      email: "",
      placeholderText: "Please enter your email here",
      error: false
    };
  },
  methods: {
    setModalVisible: function(val) {
      window.scrollTo(0, 0);
      return (this.modalVisible = val);
    },
    onChange: function(event) {
      return (this.email = event.target.value);
    },
    onSubmit: function() {
      if (!this.email) {
        this.error = true;
        return alert("Please provide your email");
      }

      if (!/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/.test(this.email)) {
        this.error = true;
        return alert("Please provide a valid email");
      }

      this.error = false;
      this.email = "";
      this.modalVisible = false;
      return alert("Awesome! 🎉🎉 Please check your email!");
    }
  }
};
</script>

<style lang="scss">
@import "../../sass/app.scss";
</style>
