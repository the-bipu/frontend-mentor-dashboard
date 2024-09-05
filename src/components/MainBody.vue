<template>
    <section class="flex w-[80%] flex-col gap-6 items-center justify-center mt-12 mb-20">

        <div
            class="flex flex-row justify-between items-center w-full h-auto text-[28px] text-black font-medium barlow">
            <span>My Challenges</span>
        </div>
        <div class="flex flex-row flex-wrap items-start justify-between">

            <div class="w-96 h-full mb-10 rounded-2xl text-[#1c2022] border border-[#dbe5e6]"
                v-for="solution in solutions.slice()" v-bind:key="solution.id">
                <!-- Project Preview -->
                <section class="rounded-t-2xl overflow-hidden innerShadow">
                    <img class="rounded-t-2xl hover:scale-110 transitionVue" v-bind:src="solution.projectPreview"
                        alt={{solution.projectName}} />
                </section>

                <div class="p-6 flex text-left h-[280px]">
                    <!-- Project Info -->
                    <section class="flex flex-col justify-between gap-4">

                        <div class="w-full h-auto flex flex-col">
                            <!-- Project Name -->
                            <p
                                class="barlow text-2xl font-medium text-[#1c2022] hover:underline transitionVue capitalize cursor-pointer mb-4">
                                {{
                                    solution.projectName }}</p>

                            <!-- Project Stack -->
                            <section class="flex flex-wrap gap-3 mb-1">
                                <p v-for="(projectStack, index) in solution.projectStack" v-bind:class="projectStack"
                                    v-bind:key="projectStack" :style="{
                                        color: index === 0 ? '#6abecd' : index === 1 ? '#3e54a3' : index === 2 ? '#cf6390' : ''
                                    }" class="font-semibold text-base barlow uppercase">
                                    {{ projectStack }}
                                </p>
                            </section>

                            <!-- Project Describtion -->
                            <section class="text-[#737373] text-base barlow font-normal leading-7">
                                <p>{{ solution.projectDescribtion }}</p>
                            </section>
                        </div>


                        <!-- Links -->
                        <section class="w-full h-auto flex flex-col">
                            <ul class="flex flex-row gap-5">
                                <li class="link-btn">
                                    <a v-bind:href="solution.liveLink" target="_blank">Live</a>
                                </li>
                                <li class="link-btn">
                                    <a v-bind:href="solution.repoLink" target="_blank">Code</a>
                                </li>
                                <li class="link-btn">
                                    <a v-bind:href="solution.projectLink" target="_blank">Solution</a>
                                </li>
                            </ul>
                        </section>

                    </section>
                </div>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    name: 'MainBody',
    props: {
        msg: String
    },
    data() {
        return {
            solutions: [
                {
                    id: 1,
                    projectName: "Job Listing with filtering",
                    projectDescribtion:
                        "In this challenge, you'll be using JavaScript to filter out jobs based on selected categories. We provide a local JSON file to help you practice working with JSON data.",
                    projectStack: ["Aurelia Js", "Tailwind", "Typescript"],
                    projectPreview: require("@/assets/preview/job-listing.jpg"),
                    liveLink:
                        "https://job-listing-aurelia.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-job-listing-application-using-aurelia-js-yqj4KDWLlw",
                    repoLink:
                        "https://github.com/the-bipu/job-listing-aurelia",
                },
                {
                    id: 2,
                    projectName: "Agency landing page",
                    projectDescribtion:
                        "This challenge will be a perfect test of your layout and responsive skills. There's a tiny bit of JS for the mobile menu, but the focus is HTML & CSS.",
                    projectStack: ["Svelte", "Tailwind", "Typescript"],
                    projectPreview: require("@/assets/preview/agency-landing.jpg"),
                    liveLink:
                        "https://sunnyside-landing-page-svelte.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-sunnyside-landing-page-using-svelte-QTuHVNk9rY",
                    repoLink:
                        "https://github.com/the-bipu/sunnyside-page-svelte",
                },
                {
                    id: 3,
                    projectName: "URL shortening API",
                    projectDescribtion:
                        "This is a perfect challenge to test your layout skills. The card layout doesn't shift, so it's also great for those that haven't dived into responsive websites yet!",
                    projectStack: ["Vue Js", "Tailwind", "Node Js"],
                    projectPreview: require("@/assets/preview/url-shortening.jpg"),
                    liveLink:
                        "https://url-shortening-vuejs.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/resposive-url-shortening-application-using-vuejs-and-tailwind-css-9Nngh-s1iZ",
                    repoLink:
                        "https://github.com/the-bipu/url-shortening-vue",
                },
                {
                    id: 4,
                    projectName: "IP Address Tracker",
                    projectDescribtion:
                        "In this challenge, you'll be using two separate APIs together to create an IP Address Tracking app.",
                    projectStack: ["Angular Js", "API"],
                    projectPreview: require("@/assets/preview/ip-tracker.jpg"),
                    liveLink:
                        "https://ip-tracker-angular-beryl.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-ip-tracker-project-using-angular-XIAzdXPUpB",
                    repoLink:
                        "https://github.com/the-bipu/ip-tracker-angular",
                },
                {
                    id: 5,
                    projectName: "Room Homepage",
                    projectDescribtion:
                        "This small homepage challenge packs a big punch to test your layout skills. There's also a slider in there to add a JS layer for extra practice.",
                    projectStack: ["React Js", "Tailwind"],
                    projectPreview: require("@/assets/preview/room-homepage.jpg"),
                    liveLink:
                        "https://room-homepage-lovat.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-room-homepage-website-vYQqVPQ1Bn",
                    repoLink:
                        "https://github.com/the-bipu/frontend-mentor-projects/tree/main/Room_HomePage",
                },
                {
                    id: 6,
                    projectName: "Advice generator app",
                    projectDescribtion:
                        "The perfect project if you're learning how to interact with 3rd-party APIs. This challenge uses the Advice Slip API to generate random quotes of advice.",
                    projectStack: ["Node Js", "Express Js", "API"],
                    projectPreview: require("@/assets/preview/advice-generator.jpg"),
                    liveLink:
                        "https://advice-generator-app-indol-five.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-advice-generator-app-using-node-and-express-ql6c1SLTZp",
                    repoLink:
                        "https://github.com/the-bipu/Advice-Generator-App",
                },
                {
                    id: 7,
                    projectName: "Todo app",
                    projectDescribtion:
                        "The classic todo app with a few twists! This app includes a dark/light theme toggle and drag & drop reordering for anyone wanting an extra test.",
                    projectStack: ["React Js", "Express Js", "MongoDb"],
                    projectPreview: require("@/assets/preview/todo-app.jpg"),
                    liveLink:
                        "https://todo-site-react.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-todo-list-app-using-react-sass-and-sanity-5vufVqoOtv",
                    repoLink:
                        "https://github.com/the-bipu/todo-app",
                },
                {
                    id: 8,
                    projectName: "Intro component with sign-up form",
                    projectDescribtion:
                        "Practice building out a sign-up form complete with client-side validation using JavaScript.",
                    projectStack: ["React Js", "Vanilla CSS", "Bootstrap"],
                    projectPreview: require("@/assets/preview/intro-signup.jpg"),
                    liveLink:
                        "https://signup-intro-component.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-signup-page-using-react-js-bootstrap-kh-vyJynXB",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/SignUp-Form-Component",
                },
                {
                    id: 9,
                    projectName: "Base Apparel coming soon",
                    projectDescribtion:
                        "This layout looks simple enough, but there are some interesting details to it that will test your CSS skills. You'll also get to practice basic form validation.",
                    projectStack: ["React Js", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/base-apparel.jpg"),
                    liveLink:
                        "https://apparel-coming-soon-page-react.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-apparel-coming-soon-page-using-react-and-bootstrap-H1xU9LzyHJ",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/Apparel-Coming-Soon-Page/current-files",
                },
                {
                    id: 10,
                    projectName: "Ping single column coming soon",
                    projectDescribtion:
                        "This challenge is great for beginners and offers a chance to practice basic client-side form validation.",
                    projectStack: ["React Js", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/ping-page.jpg"),
                    liveLink:
                        "https://ping-coming-soon-page-react.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-ping-coming-soon-page-using-react-ye5a57VsEd",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/Ping-Coming-Soon-Page",
                },
                {
                    id: 11,
                    projectName: "Age calculator app",
                    projectDescribtion:
                        "This challenge is designed to sharpen your JavaScript and form validation skills. Working with dates in JavaScript can be tricky, so this will be a nice test!",
                    projectStack: ["React Js", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/age-cal.jpg"),
                    liveLink:
                        "https://age-calculator-module.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-age-calculator-app-using-react-js-pTsfTuUi98",
                    repoLink:
                        "https://github.com/the-bipu/Age-Calculator-App",
                },
                {
                    id: 12,
                    projectName: "FAQ accordion card",
                    projectDescribtion:
                        "In this challenge, you'll be building out an FAQ accordion. This is an extremely common front-end pattern, so it's a great opportunity to get some practice in!",
                    projectStack: ["JQuery", "Bootstrap"],
                    projectPreview: require("@/assets/preview/faqs-page.jpg"),
                    liveLink:
                        "https://faq-accordion-the-bipu.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-faq-accordion-card-using-flexbox-grid-fUSnZS8N4s",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/FAQ-Accordion",
                },
                {
                    id: 13,
                    projectName: "Interactive rating component",
                    projectDescribtion:
                        "This is a nice, small project to practice handling user interactions and updating the DOM. Perfect for anyone who has learned the basics of JavaScript!",
                    projectStack: ["JQuery", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/rating-component.jpg"),
                    liveLink:
                        "https://rating-component-the-bipu.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-rating-component-using-jquery-flexbox-and-grid-7zhyLMmMAG",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/Rating-Component-Vanilla",
                },
                {
                    id: 14,
                    projectName: "Testimonials grid section",
                    projectDescribtion:
                        "This challenge will be perfect practice for anyone wanting to test their CSS Grid skills. Grid is such a powerful addition to CSS, so it's worth getting to grips with it!",
                    projectStack: ["React Js", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/testimonial.jpg"),
                    liveLink:
                        "https://testimonial-grid-challenge-thebipu.vercel.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/fully-responsive-testimonial-grid-card-using-react-grid-and-flexbox-R7cfvFXN5p",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/Testimonial-Grid-Component/current-files",
                },
                {
                    id: 15,
                    projectName: "NFT preview card component",
                    projectDescribtion:
                        "This HTML & CSS only challenge is perfect for anyone just starting out or anyone wanting a small project to play around with.",
                    projectStack: ["HTML", "Vanilla CSS"],
                    projectPreview: require("@/assets/preview/nft-card.jpg"),
                    liveLink:
                        "https://nft-card-the-bipu.netlify.app/",
                    projectLink:
                        "https://www.frontendmentor.io/solutions/responsive-nft-preview-card-using-grid-and-flexbox-iqalU54NH7",
                    repoLink:
                        "https://github.com/the-bipu/Frontend-Mentor-Projects/tree/main/NFT-Card-Component",
                },
            ],
        };
    },
};
</script>