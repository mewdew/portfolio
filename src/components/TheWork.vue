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
              img: "./assets/p1_rx.png",
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
              id: "ix",
              header: "Ideation",
              img: "",
              main: "I created paper wireframes to iterate over multiple options and then moved on to digital ones for usability testing.",
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
              header: "Usability Tests",
              img: "./assets/p1_tx.png",
              main: "I conducted 2 rounds of usability studies that lead that helped revise some design choices to better suit the user base.",
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
                  content: "",
                  img: "./assets/p1_impact.png",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "",
                  img: "./assets/p1_wil.png",
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
              img: "./assets/p2_rx.png",
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
              header: "Usability Tests",
              img: "./assets/p2_tx.png",
              main: "I conducted 2 rounds of usability studies that lead that helped revise some design choices to better suit the user base.",
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
                  content: "",
                  img: "./assets/p2_impact.png",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "",
                  img: "./assets/p2_wil.png",
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
              img: "./assets/p3_rx.png",
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
              id: "tx",
              header: "Usability Tests",
              img: "./assets/p3_tx.png",
              main: "I conducted 2 rounds of usability studies that lead that helped revise some design choices to better suit the user base.",
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
                  content: "",
                  img: "./assets/p3_impact.png",
                },
                {
                  id: "s2",
                  header: "What I learned",
                  content: "",
                  img: "./assets/p3_wil.png",
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
    <div
      class="project"
      v-for="item in projects"
      :key="item.id"
      @click="
        activeIdx = item.id;
        activeItem = projects[activeIdx - 1];
      "
    >
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
    <h3>{{ activeItem.header }} : {{ activeItem.description }}</h3>
    <div
      class="projectInfo flexCol"
      v-for="(b, index) of activeItem.body"
      :key="index"
    >
      <div class="contentWrapper flexRow">
        <div class="leftSection">
          <img v-if="b.img" v-bind:src="b.img" alt="bImg" />
        </div>
        <div class="rightSection flexCol">
          <div class="main">{{ b.main }}</div>
          <div
            class="section flexRow"
            v-for="section of b.sections"
            v-bind:key="section.id"
          >
            <div class="header">{{ section.header }}</div>
            <img v-if="section.img" v-bind:src="section.img" alt="sectionImg" />
            <div class="content">{{ section.content }}</div>
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
}
.flexRow {
  display: flex;
  flex-direction: row;
}
h3 {
  text-align: center;
  padding: 1rem; /* IE6-9 */
}
h4 {
  text-align: center;
  padding: 1rem;
  background: rgb(0, 0, 0);
  color: #f1f1f1;
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
  background: #c5cce9; /* Old browsers */
  background: -moz-linear-gradient(
    top,
    #c5cce9 0%,
    #c5cce9 33%,
    #efe3ef 33%,
    #efe3ef 66%,
    #eec7c8 66%,
    #eec7c8 100%
  ); /* FF3.6-15 */
  background: -webkit-linear-gradient(
    top,
    #c5cce9 0%,
    #c5cce9 33%,
    #efe3ef 33%,
    #efe3ef 66%,
    #eec7c8 66%,
    #eec7c8 100%
  ); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(
    to bottom,
    #c5cce9 0%,
    #c5cce9 33%,
    #efe3ef 33%,
    #efe3ef 66%,
    #eec7c8 66%,
    #eec7c8 100%
  ); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#c5cce9', endColorstr='#eec7c8',GradientType=0 );
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
}
.leftSection img {
  height: 35vh;
}
.rightSection img {
  height: 20vh;
}
</style>
