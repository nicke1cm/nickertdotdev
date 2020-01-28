<template>
  <div class="coverLetterModal">
    <mdb-container>
      <!-- poll modal -->
      <mdb-modal :show="poll" @close="closePoll" info fullHeight>
        <mdb-modal-header center :close="true" class="ripe-malinka-gradient">
          <p class="heading">
            <i class="fas fa-file-signature text-white mr-1"></i> Generate My Cover Letter
          </p>
        </mdb-modal-header>
        <mdb-modal-body class="elegant-color">
          <p class="text-center pink-text">
            <strong>Job Details</strong>
          </p>
          <mdb-input
            id="jobTitle"
            autocomplete="off"
            type="text"
            class="mb-2 mt-0"
            label="Job Title"
            v-model="title"
          ></mdb-input>
          <mdb-input
            id="jobCompany"
            autocomplete="off"
            type="text"
            class="mb-2 mt-0"
            label="Company"
            v-model="jobCompany"
          ></mdb-input>
          <mdb-input
            id="jobUrl"
            autocomplete="off"
            type="text"
            class="mb-2 mt-0"
            label="Job URL"
            v-model="link"
          ></mdb-input>
        </mdb-modal-body>
        <mdb-modal-footer center class="elegant-color-dark border-0">
          <mdb-btn
            class="ripe-malinka-gradient"
            @click="submit"
            icon="file-download"
            iconRight
            iconClass="ml-1 white-text"
          >Generate</mdb-btn>
          <mdb-btn color="light" @click="closePoll">Cancel</mdb-btn>
        </mdb-modal-footer>
      </mdb-modal>
    </mdb-container>
  </div>
</template>

<script>
import {
  mdbContainer,
  mdbBtn,
  mdbModal,
  mdbModalHeader,
  mdbModalBody,
  mdbModalFooter
} from "mdbvue";
export default {
  name: "CoverLetterModal",
  components: {
    mdbContainer,
    mdbBtn,
    mdbModal,
    mdbModalHeader,
    mdbModalBody,
    mdbModalFooter
  },
  props: {
    poll: Boolean
  },
  data: () => {
    return { min: "", max: "" };
  },
  methods: {
    closePoll: function() {
      this.$emit("coverLetterModalToggleEmit", false);
    },
    submit: function() {
      this.closePoll();
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.coverLetterModal {
  .md-form input:focus,
  .md-form textarea:focus {
    box-shadow: 0 1px 0 0 #e91e63 !important;
    border-bottom: 1px solid #e91e63 !important;
    color: white;
  }

  .md-form input,
  .md-form textarea {
    color: #9e9e9e;
  }

  .md-form label.active {
    color: #e91e63 !important;
  }
}
</style>
