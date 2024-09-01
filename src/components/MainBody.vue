<template>
    <section class="flex w-[80%] flex-col gap-6 items-center justify-center my-20">

        <div class="flex flex-row flex-wrap items-start justify-between">
            <div class="w-96 h-full mb-10 rounded-2xl text-[#1c2022] border border-[#dbe5e6]"
                v-for="solution in solutions.slice().reverse()" v-bind:key="solution.id">
                <!-- Project Preview -->
                <section class="rounded-t-2xl overflow-hidden innerShadow">
                    <img class="rounded-t-2xl hover:scale-110 transitionVue" v-bind:src="solution.projectPreview"
                        alt={{solution.projectName}} />
                </section>

                <div class="p-6 flex text-left h-[250px]">
                    <!-- Project Info -->
                    <section class="flex flex-col justify-between gap-4">

                        <div class="w-full h-auto flex flex-col gap-4">
                            <!-- Project Name -->
                            <p class="barlow text-2xl font-medium text-[#1c2022] hover:underline transitionVue capitalize cursor-pointer">{{
                                solution.projectName }}</p>

                            <!-- Project Describtion -->
                            <section class="text-[#737373] text-base barlow font-normal leading-7">
                                <p>{{ solution.projectDescribtion }}</p>
                            </section>
                        </div>

                        <!-- Project Stack -->
                        <!-- <section class="flex flex-wrap gap-2">
                            <p class="project-stack" v-for="projectStack in solution.projectStack"
                                v-bind:class="projectStack" v-bind:key="projectStack">
                                {{ projectStack }}
                            </p>
                        </section> -->

                        <!-- Links -->
                        <section class="w-full h-auto flex flex-col">
                            <ul class="flex flex-row gap-5">
                                <li class="link-btn">
                                    <a v-bind:href="solution.liveLink" target="_blank">Live</a>
                                </li>
                                <li class="link-btn">
                                    <a v-bind:href="solution.repoLink" target="_blank">Repo</a>
                                </li>
                                <li class="link-btn">
                                    <a v-bind:href="solution.projectLink" target="_blank">Try Out</a>
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
                    projectName: "Stats Preview Card",
                    projectDescribtion:
                        "This is a great small challenge to help get you used to building to a design. There's no JS in this project, so you'll be able to focus on your HTML & CSS skills.",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/stats-preview-card-component.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "https://github.com/catherineisonline/stats-preview-card-component-frontendmentor",
                },
                {
                    id: 2,
                    projectName: "Order summary component",
                    projectDescribtion:
                        "A perfect project for newbies who are starting to build confidence with layouts!",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/order-summary-component.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 3,
                    projectName: "Profile card component",
                    projectDescribtion:
                        "This is a perfect challenge to test your layout skills. The card layout doesn't shift, so it's also great for those that haven't dived into responsive websites yet!",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/profile-card-component.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 4,
                    projectName: "Single price grid",
                    projectDescribtion:
                        "In this challenge, you will build out the pricing component to the designs provided. This is perfect for beginners and people who want to complete a smaller challenge.",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/single-price-grid-component.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 5,
                    projectName: "3-column preview card",
                    projectDescribtion:
                        "This challenge is perfect if you're just getting started. The shift between the layouts will be a nice test if you're new to building responsive projects.",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/3-column-preview-card-component.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 6,
                    projectName: "Social proof section",
                    projectDescribtion:
                        "This project will test your layout skills. If you're starting to get confident with Flexbox or Grid, this will provide a nice challenge!",
                    projectStack: ["HTML", "CSS"],
                    projectPreview: require("@/assets/images/social-proof-section.jpeg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
            ],
        };
    },
};
</script>