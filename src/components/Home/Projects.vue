<template>
  <div class="projects">
    <mdb-card class="mt-3">
      <mdb-list-group>
        <mdb-list-group-item>
          <mdb-card-body class="m-0 pb-1">
            <a v-on:click="openPanel(0)" class="d-flex justify-content-between">
              <strong>Basic card</strong>
              <i
                :class="isPanelOpen(0)? 'fa-chevron-up': 'fa-chevron-down'"
                class="pink-text fas fa-2x"
              ></i>
            </a>
            <div :class="isPanelOpen(0)? 'open': 'closed'" class="accordion-body">
              <mdb-card-text
                class="pt-4"
              >Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
              <a href="#">View Project</a>
            </div>
          </mdb-card-body>
        </mdb-list-group-item>

        <mdb-list-group-item>
          <mdb-card-body class="m-0 pb-1">
            <a v-on:click="openPanel(1)" class="d-flex justify-content-between">
              <strong>Basic card</strong>
              <i
                :class="isPanelOpen(1)? 'fa-chevron-up': 'fa-chevron-down'"
                class="pink-text fas fa-2x"
              ></i>
            </a>
            <div :class="isPanelOpen(1)? 'open': 'closed'" class="accordion-body">
              <mdb-card-text
                class="pt-4"
              >Some quick example text to build on the card title and make up the bulk of the card's content.</mdb-card-text>
              <a href="#">View Project</a>
            </div>
          </mdb-card-body>
        </mdb-list-group-item>
      </mdb-list-group>
    </mdb-card>
  </div>
</template>

<script>
import {
  mdbCard,
  mdbCardText,
  mdbCardBody,
  mdbListGroup,
  mdbListGroupItem
} from "mdbvue";
export default {
  name: "Projects",
  components: {
    mdbCard,
    mdbCardText,
    mdbCardBody,
    mdbListGroup,
    mdbListGroupItem
  },
  data: () => {
    return {
      currentOpenPanels: ""
    };
  },
  methods: {
    openPanel: function(panelIndex) {
      if (this.isPanelOpen(panelIndex)) {
        this.currentOpenPanels = this.currentOpenPanels.replace(
          panelIndex.toString(),
          ""
        );
      } else {
        this.currentOpenPanels += panelIndex;
      }
    },
    isPanelOpen: function(panelIndex) {
      return this.currentOpenPanels.indexOf(panelIndex.toString()) > -1;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.accordion-body {
  transition: max-height 0.3s ease-out;
}

.closed {
  max-height: 0px;
  overflow: hidden;
}

.open {
  max-height: 200px;
  overflow: hidden;
}
</style>
