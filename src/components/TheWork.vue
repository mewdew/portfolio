<script lang="ts">
import { defineComponent } from "vue";

interface Content {
  id: string;
  header?: string;
  content?: string;
  img?: string;
}

interface MainContent {
  id: string;
  header?: string;
  img?: string;
  main?: string;
  sections?: Array<Content>;
}

export interface ProjectItem {
  id?: number;
  header?: string;
  description?: string;
  body?: Array<MainContent>;
}

export default defineComponent({
  // type inference enabled
  props: {
    msg: { type: String },
  },
  data() {
    return {
      activeIdx: 0,
      activeItem: ((item: ProjectItem): ProjectItem => {
        return item ? item : {};
      })({}),
      projects: [
        {
          id: 1,
          header: "NutriCal",
          description: "Healthy food at your doorstep.",
          img: "./assets/project1.png",
          body: [
            {
              id: "ov",
              header: "Overview",
              img: "./assets/p1_ov.png",
              main: "NutriCal is health-centric food ordering app. We help our users make informed choices when it comes to food. Our users can explore the nutrient profile, customize the ingredients to suit their health goals.",
              sections: [
                {
                  id: "s1",
                  header: "Problem",
                  content:
                    "We are helping our users get a clearer picture of what the eat. The offerings on the platform focuses on the need and concerns of the users.",
                },
                {
                  id: "s2",
                  header: "Goal",
                  content:
                    "Our goal is to help users make informed and healthy food choices.",
                },
              ],
            },
            {
              id: "rx",
              header: "Research",
              img: "",
              main: "We found the following user pain paints upon conducting UX reserach.",
              sections: [
                {
                  id: "s1",
                  header: "Time",
                  content: "A lot of adults find it difficult to make time to cook twice a day.",
                  img: "",
                },
                {
                  id: "s2",
                  header: "Lack of Choices",
                  content: "Though there are multiple food ordering apps but gluttony is glorified and there’s a lack of healthy choices.",
                  img: "",
                },
                {
                  id: "s3",
                  header: "Health Concerns",
                  content: "A sizeable group of people find it difficult to order food that can be customized to address their health concerns",
                  img: "",
                },
                {
                  id: "s4",
                  header: "Lack of Clarity",
                  content: "There’s a lot of misinformation regarding what’s healthy and what’s not.",
                  img: "",
                },
              ],
            },
            {
              id: "ix",
              header: "Ideation",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Paper Wireframes",
                  content: "",
                  img: "./assets/p1_pwf.png",
                },
                {
                  id: "s2",
                  header: "Digital Wireframes",
                  content: "",
                  img: "./assets/p1_lfp.png",
                },
              ],
            },
            {
              id: "tx",
              header: "Usability Test Findings",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Round 1",
                  content: `1. Login step was cumbersome.\n2. User wanted additional customizations.\n3. Main user flow lacked easy back and forth navigation`,
                  img: "",
                },
                {
                  id: "s2",
                  header: "Round 2",
                  content: `1. Users wanted an ETA on the delivery.\n2. Users wanted flexibility in payment choices`,
                  img: "",
                },
              ],
            },
            {
              id: "mu",
              header: "MockUps",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Main User Flow",
                  content: "",
                  img: "./assets/p1_muf.png",
                },
                {
                  id: "s2",
                  header: "High Fidelity Prototype",
                  content: "",
                  img: "./assets/p1_hfp.png",
                },
              ],
            },
            {
              id: "cx",
              header: "Conclusion",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Impact",
                  content: "The app caters to user’s preferences and induces a sense of control over the ordering flow. Wd got a lot of positive feedback from the usability tests pertaining to viability of the app.",
                  img: "",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "While designing the NutriCal app, I learned something new at each step of the way. I understood the importance of accessibility, information architecture and design principles that must be kept in mind to deliver intuitive designs. Users and Peer feedback helped in materialising the final outcome.",
                  img: "",
                },
              ],
            },
          ],
        },
        {
          id: 2,
          header: "Optrade",
          description: "Gateway to F&O trading.",
          img: "./assets/project2.png",
          body: [
            {
              id: "ov",
              header: "Overview",
              img: "./assets/p2_ov.png",
              main: "OpTrade provides analytical tools to traders who invest in the Futures & Options segment. It has offerings for both beginners as well as seasoned investors.",
              sections: [
                {
                  id: "s1",
                  header: "Problem",
                  content:
                    "We are helping our traders make wise decision backed by data analytics. The offerings on the platform focuses on the need and concerns of the investors.",
                },
                {
                  id: "s2",
                  header: "Goal",
                  content:
                    "Our goal is to help users make informed investment choices.",
                },
              ],
            },
            {
              id: "rx",
              header: "Research",
              img: "",
              main: "We found the following user pain paints upon conducting UX reserach.",
              sections: [
                {
                  id: "s1",
                  header: "Time",
                  content: "A lot of adults find it difficult to make time to collate all data required.",
                  img: "",
                },
                {
                  id: "s2",
                  header: "Lack of Awareness",
                  content: "TSome beginners as well as seasoned investors were surprised when the saw the indices and events we were tracking as they were not aware of them at all.",
                  img: "",
                },
                {
                  id: "s3",
                  header: "Risk Concerns",
                  content: "A sizeable group of people find it difficult to weigh risk associated with their decision.",
                  img: "",
                },
                {
                  id: "s4",
                  header: "Information Overload",
                  content: "There’s a lot of information out there and it’s difficult to filter out what’s important.",
                  img: "",
                },
              ],
            },
            {
              id: "ix",
              header: "Ideation",
              img: "",
              main: "I created paper wireframes to iterate over multiple options and then moved on to digital ones for usability testing.",
              sections: [
                {
                  id: "s1",
                  header: "Paper Wireframes",
                  content: "",
                  img: "./assets/p2_pwf.png",
                },
                {
                  id: "s2",
                  header: "Digital Wireframes",
                  content: "",
                  img: "./assets/p2_lfp.png",
                },
              ],
            },
            {
              id: "tx",
              header: "Usability Test Findings",
              img: "",
              main: "I conducted 2 rounds of usability studies that lead that helped revise some design choices to better suit the user base.",
              sections: [
                {
                  id: "s1",
                  header: "Round 1",
                  content: `1. User found the UX for mobile version cluttered.\n2. Main user flow lacked easy back and forth navigation`,
                  img: "",
                },
                {
                  id: "s2",
                  header: "Round 2",
                  content: `1. User wanted a way to submit questions/queries.\n2. Users wanted flexibility in payment choices`,
                  img: "",
                },
              ],
            },
            {
              id: "mu",
              header: "MockUps",
              img: "",
              main: "After the usability study, navigation flow was revised and consistent tabbed footer menu was added to avoid loss of context for user.",
              sections: [
                {
                  id: "s1",
                  header: "Main User Flow",
                  content: "",
                  img: "./assets/p2_muf.png",
                },
                {
                  id: "s2",
                  header: "High Fidelity Prototype",
                  content: "",
                  img: "./assets/p2_hfp.png",
                },
              ],
            },
            {
              id: "cx",
              header: "Conclusion",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Impact",
                  content: "The app caters to user’s preferences and induces a sense of confidence regarding the investment choice they make. It caters to a niche group of people who will find this app very useful.",
                  img: "",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "While designing the OpTrade website, I learned something new at each step of the way. I understood the importance of accessibility, information architecture and design principles that must be kept in mind to deliver intuitive designs. Users and Peer feedback helped in materialising the final outcome.",
                  img: "",
                },
              ],
            },
          ],
        },
        {
          id: 3,
          header: "YouThePeople",
          description: "Bridge between You and the Government.",
          img: "./assets/project3.png",
          body: [
            {
              id: "ov",
              header: "Overview",
              img: "./assets/p3_ov.png",
              main: "A citizen centric hyper-local social networking platform that informs users of latest policy updates, find volunteering and engagement opportunities with the government programmes.",
              sections: [
                {
                  id: "s1",
                  header: "Problem",
                  content:
                    "The government and the citizen need to act together for effective policy implementation. This requires citizens to be aware of their rights and duties and have access to a platform which could also serve as a system of check and balance.",
                },
                {
                  id: "s2",
                  header: "Goal",
                  content:
                    "Bridge the gap between policy formulation and implementation. Give citizens a platform to connect and organize themselves, stay informed of the latest programmes and schemes put forth by the government.",
                },
              ],
            },
            {
              id: "rx",
              header: "Research",
              img: "",
              main: "I conducted user interviews and used empathy maps to arrive at insights that I could incorporate in my designs. The user base comprised of citizens aged 18 yrs of age and above (those who can exercise their voting rights). The user group confirmed our assumption about the gap that exists between policy formulation and implementation and the lack of awareness among citizens. The research further help gain clarity in what would incentivize citizens to use the platform to become a harbinger of change.",
            },
            {
              id: "ix",
              header: "Ideation",
              img: "",
              main: "I created paper wireframes to iterate over multiple options and then moved on to digital ones for usability testing.",
              sections: [
                {
                  id: "s1",
                  header: "Paper Wireframes",
                  content: "",
                  img: "./assets/p3_pwf.png",
                },
                {
                  id: "s2",
                  header: "Digital Wireframes",
                  content: "",
                  img: "./assets/p3_lfp.png",
                },
              ],
            },
            {
              id: "mu",
              header: "MockUps",
              img: "",
              main: "After the usability study, navigation flow was revised and consistent tabbed footer menu was added to avoid loss of context for user.",
              sections: [
                {
                  id: "s1",
                  header: "Main User Flow",
                  content: "",
                  img: "./assets/p3_muf.png",
                },
                {
                  id: "s2",
                  header: "High Fidelity Prototype",
                  content: "",
                  img: "./assets/p3_hfp.png",
                },
              ],
            },
            {
              id: "cx",
              header: "Conclusion",
              img: "",
              main: "",
              sections: [
                {
                  id: "s1",
                  header: "Impact",
                  content: "There is no platform like YouThePeople that citizen centric and provides hyper local content and options to engage. The positive feedback from the usability studies is a testament to its potential.",
                  img: "",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "While designing the YouThePeople platform,I learned something new at each step of the way. I understood the importance of accessibility, information architecture and design principles that must be kept in mind to deliver intuitive designs. Users and Peer feedback helped in materialising the final outcome.",
                  img: "",
                },
              ],
            },
          ],
        },
      ],
    };
  },
  //
  mounted() {
    this.activeIdx; // type: string | undefined
    this.activeItem; // type: ProjectItem | undefined
    this.msg; // type: string
    this.projects; // type: array
  },
  // components: { WelcomeItem },
});
</script>

<template>
  <h3>
    <span :class="{ active: activeIdx > 0 }" @click="activeIdx = 0">
      Projects
    </span>
    <span v-if="activeIdx"> / {{ projects[activeIdx - 1]["header"] }}</span>
  </h3>
  <div v-if="!activeIdx" class="projects">
    <div class="project" v-for="item in projects" :key="item.id" @click="
      activeIdx = item.id;
    activeItem = projects[activeIdx - 1];
    ">
      <h4>{{ item.header }}</h4>
      <div class="img">
        <img v-bind:src="item.img" alt="image" />
      </div>
      <div class="desc">
        <p>{{ item.description }}</p>
      </div>
    </div>
  </div>
  <div v-if="activeIdx" class="activeProject flexCol">
    <h2>{{ activeItem.header }} : {{ activeItem.description }}</h2>
    <div class="projectInfo flexCol" v-for="(b, index) of activeItem.body" :key="index">
      <div v-if="b.header" class="header">{{ b.header }}</div>
      <div class="contentWrapper flexRow">
        <div class="leftSection">
          <img v-if="b.img" v-bind:src="b.img" alt="bImg" />
        </div>
        <div class="rightSection flexCol">
          <div class="main">{{ b.main }}</div>
          <div class="sections flexRow">
            <div class="section flexCol" v-for="section of b.sections" v-bind:key="section.id">
              <div class="header">{{ section.header }}</div>
              <img v-if="section.img" v-bind:src="section.img" alt="sectionImg" />
              <div class="content">
                <pre>{{ section.content }}</pre>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.flexCol {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

.flexRow {
  display: flex;
  flex-direction: row;
}

h3 {
  text-align: center;
  padding: 1rem;
  /* IE6-9 */
}

h2 {
  padding: 2rem;
}

h4 {
  text-align: center;
  padding: 1rem;
  background: rgb(0, 0, 0);
  color: #f1f1f1;
}
pre {
  white-space: break-spaces;
  font-family: inherit;
}

span.active {
  color: #00bd7e;
  cursor: pointer;
}

.projects {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.project {
  position: relative;
  display: flex;
  flex-direction: column;
  flex: 1 1 30vw;
  margin: 1rem;
  box-shadow: 0 4px 8px 0 rgb(0 0 0 / 20%), 0 6px 20px 0 rgb(0 0 0 / 19%);
  cursor: pointer;
  background: #c5cce9;
  /* Old browsers */
  background: -moz-linear-gradient(top,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%);
  /* FF3.6-15 */
  background: -webkit-linear-gradient(top,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%);
  /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(to bottom,
      #c5cce9 0%,
      #c5cce9 33%,
      #efe3ef 33%,
      #efe3ef 66%,
      #eec7c8 66%,
      #eec7c8 100%);
  /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#c5cce9', endColorstr='#eec7c8', GradientType=0);
}

.img {
  height: inherit;
  width: inherit;
  padding: 1rem;
}

img {
  max-width: 100%;
  max-height: 100%;
}

.desc {
  position: absolute;
  bottom: 0;
  background: rgba(0, 0, 0, 0.7);
  color: #f1f1f1;
  width: 100%;
  text-align: center;
  padding: 1rem;
}

.activeProject {
  display: flex;
  flex-direction: column;
  width: 80%;
  margin: 0 auto;
  padding-bottom: 4rem;
}

div.header {
  font-style: italic;
  font-weight: 500;
}

div.main {
  padding-bottom: 3rem;
}

.projectInfo {
  padding: 2rem 0;
}

.section div.header {
  font-weight: normal;
}

.leftSection {
  padding: 0 1rem;
}

.contentWrapper {
  justify-content: center;
  padding: 1rem;
}

.section {
  flex: 1;
  padding: 0 0.5rem;
}
</style>
