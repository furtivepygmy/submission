<template>
    <div class="container">
        <div class="section">
            <h2 class="section__title">
                10 Best Photo Apps For Incredible iPhone Photography (2020
                Edition)
            </h2>
            <!-- <hr class="gradient" /> -->
            <div class="section__divider" />
            <p class="section__text">
                How do you capture more interesting travel photos with your
                iPhone? How do you avoid taking the same cliché vacation photos
                that everyone else takes? I recently interviewed Steffen Geldner
                - a talented iPhone photographer with a passion for travel. In
                this article, Steffen reveals 7 tips for shooting beautiful
                travel photos that will preserve the amazing memories of your
                trip. Read on to discover how to take better travel photos with
                your iPhone!
            </p>
            <!-- <div class="section__image-container-mask"></div> -->
            <div class="section__image-container"></div>
            <h2 class="section__subtitle">
                1. Research Your Destination To Find The Best Photo
                Opportunities
            </h2>
            <p class="section__text">
                Before your trip, I recommend researching the destination to
                find the most interesting photo opportunities.
                <br />
                <br />
                I always research the location I'm traveling to. I do this
                extensively and obsessively!
                <br />
                <br />
                It's up to you how much research you do. But you should
                definitely spend a bit of time looking up some great places to
                take pictures.
                <br />
                <br />
                So. what kind of research can you do?
                <br />
                <br />
                First, you could search for photos that other people have taken
                at the locations you're planning to visit.
                <br />
                <br />
                Search on Instagram or Google to get an idea of the kinds of
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
                <br />
                For a more complete photographic story, capture your journey to
                and from the location you're visiting.
                <br />
                <br />
                If you're traveling by plane. try to get a window seat where you
                have a view of the wing or propeller.
                <br />
                <br />
                And of course, you could capture a beautiful aerial view of
                clouds, mountains, or city lights as you're flying above.
                <br />
                <br />
                Your journey will often involve several different types of
                transport. And they all offer great photo opportunities.
                <br />
                <br />
                Whether you're traveling by car, taxi, bus, train, boat, or
                plane, try to capture some interesting photos.
            </p>
        </div>
        <div class="sidebar"><Button title="Send Me The Tips" /></div>
    </div>
</template>

<script>
Vue.component("Button", {
    props: ["title"],
    template: '<button class="sidebar__gradient-button" >{{ title }}</button>'
});

export default {};
</script>

<style lang="scss">
@import "../../sass/app.scss";
</style>
