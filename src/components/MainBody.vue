<template>
    <section class="flex w-[80%] flex-col gap-6 items-center justify-center my-20">

        <div
            class="flex flex-row justify-between items-center w-full h-auto text-[28px] text-black font-semibold barlow">
            <span>My Challenges</span>
        </div>
        <div class="flex flex-row flex-wrap items-start justify-between">

            <div class="w-96 h-full mb-10 rounded-2xl text-[#1c2022] border border-[#dbe5e6]"
                v-for="solution in solutions.slice().reverse()" v-bind:key="solution.id">
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
                    projectName: "Job Listing with filtering",
                    projectDescribtion:
                        "In this challenge, you'll be using JavaScript to filter out jobs based on selected categories. We provide a local JSON file to help you practice working with JSON data.",
                    projectStack: ["Aurelia Js", "Tailwind", "Typescript"],
                    projectPreview: require("@/assets/preview/job-listing.jpg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 2,
                    projectName: "Agency landing page",
                    projectDescribtion:
                        "This challenge will be a perfect test of your layout and responsive skills. There's a tiny bit of JS for the mobile menu, but the focus is HTML & CSS.",
                    projectStack: ["Svelte", "Tailwind", "Typescript"],
                    projectPreview: require("@/assets/preview/agency-landing.jpg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 3,
                    projectName: "URL shortening API",
                    projectDescribtion:
                        "This is a perfect challenge to test your layout skills. The card layout doesn't shift, so it's also great for those that haven't dived into responsive websites yet!",
                    projectStack: ["Vue Js", "Tailwind", "Node Js"],
                    projectPreview: require("@/assets/preview/url-shortening.jpg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 4,
                    projectName: "IP Address Tracker",
                    projectDescribtion:
                        "In this challenge, you'll be using two separate APIs together to create an IP Address Tracking app.",
                    projectStack: ["Angular Js", "API"],
                    projectPreview: require("@/assets/preview/ip-tracker.jpg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 5,
                    projectName: "Room Homepage",
                    projectDescribtion:
                        "This small homepage challenge packs a big punch to test your layout skills. There's also a slider in there to add a JS layer for extra practice.",
                    projectStack: ["React Js", "Tailwind"],
                    projectPreview: require("@/assets/preview/room-homepage.jpg"),
                    liveLink:
                        "",
                    projectLink:
                        "",
                    repoLink:
                        "",
                },
                {
                    id: 6,
                    projectName: "Advice generator app",
                    projectDescribtion:
                        "The perfect project if you're learning how to interact with 3rd-party APIs. This challenge uses the Advice Slip API to generate random quotes of advice.",
                    projectStack: ["Node Js", "Express Js", "API"],
                    projectPreview: require("@/assets/preview/advice-generator.jpg"),
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