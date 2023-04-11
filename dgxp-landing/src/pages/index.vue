<template>
  <div class="root">
    <LandingHeader />

    <div class="floating-btn">
      <FloatingForm :show-form="showForm" />
      <FloatingButton @toggleShowForm="updateShowForm" />
    </div>

    <HeroSection @toggleShowForm="updateShowForm" />

    <BenefitSection />

    <ApplicationSection />

    <FeatureSection />

    <LandingFooter />
  </div>
</template>

<script>
import LandingHeader from "../components/LandingHeader.vue";
import HeroSection from "../components/HeroSection.vue";
import FloatingForm from "../components/FloatingForm.vue";
import FloatingButton from "../components/FloatingButton.vue";
import BenefitSection from "../components/BenefitSection.vue";
import ApplicationSection from "../components/ApplicationSection.vue";
import FeatureSection from "../components/FeatureSection.vue";
import LandingFooter from "../components/LandingFooter.vue";

import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "IndexPage",
  created() {
    AOS.init();
  },
  data() {
    return {
      title: "Digital GxP - Digital Documentation towards Pharma 4.0",
      emailForDemo: null,
      showForm: false,
    };
  },
  head() {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { charset: "utf-8" },
        { name: "viewport", content: "width=device-width, initial-scale=1" },
        {
          hid: "description",
          name: "description",
          content:
            "Complete end to end Digitalization towards a Paperless Platform. Plan, document and organise your experiments with ease and efficiency",
        },
        {
          hid: "keywords",
          name: "keywords",
          content:
            "Notes, SOP, Log, Books, Protocols, Batch Records, Check, Sheets, Work Orders, Forms, ELN, Standard practices, Digital SOP, SOP, Electronic Documentation, GxP,Process Documentation, Workflow, Protocol, Testing protocol, Electronic form, E-forms, Electronic Batch Records, Batch records, Industry 4.0, Digital Transformation, Laboratory procedure, GLP, Laboratory automation, Laboratory digitization, Contract Laboratory, Assay procedure, Testing procedure, Data integrity, Traceability, Human Errors, Paperless, QC, Verification, QA, Quality Control, Quality Management, QMS, HIPAA, GMP, Biopharma, Biotech, Biologics, Manufacturing, Pharmaceutical Manufacturing, CRO, CLO, CMO, CDMO, Clinical research, Analysis, Analyst, Analytical procedure, DMS, Document Management System, LIMS, Laboratory Information Management System, FDA, EMEA, Pharmacopeia, Good Documentation Practice, Maintainence, Scheduling, Operator, Operator training, Technologist, Hands-on, Equipment, On-site, On-site training, Operational Excellence, OE, OEM, FMEA, Experiment, Outsource, Operator training, Troubleshooting, Trackwise, Video SOP, Academic Research Lab, Vendor training, Verification, Visual Inspection, Food Safety , Satellite labs, CLIA certified laboratory, CLIA, Clinical diagnostics, Validation, Assay validation, Environmental Testing, Instrument tool, Manual, Installation, User manual, High end manufacturing, Preventive Maintainence, PM, Failure Mode Analysis, Subject Matter Expert, Supervisor, Supervision, Oversight, Punchlist, Turnover Packages, Subcontract, On-site testing, FAT, Factory Acceptance Test, SAT, Site Acceptance Test, Information Management System, Computer System Validation, Task list, Checklist, Process Management, Deviation, CAPA, Electronic Signatures, Audit Trail, FDA Compliance, Lean, Six Sigma, 21 CFR Compliance Part 11, cGMP, Compliance Management, Good Working Practice, Commissioning, Instrument Demo, Qualification, Operational Qualification, Performance Qualification, Field service engineer, Audit, FDA Audit, FDA Warnings, Standardisation, Reference, Cross reference",
        },
      ],
    };
  },
  components: {
    LandingHeader,
    HeroSection,
    FloatingForm,
    FloatingButton,
    BenefitSection,
    ApplicationSection,
    FeatureSection,
    LandingFooter,
  },
  methods: {
    updateShowForm: function () {
      this.showForm = !this.showForm;
    },
  },
};
</script>

<style>
@font-face {
  font-family: "Poppins";
  src: url("../assets/fonts/Poppins/Poppins-Regular.ttf");
  font-weight: normal;
  font-display: swap;
}

@font-face {
  font-family: "Poppins";
  src: url("../assets/fonts/Poppins/Poppins-Bold.ttf");
  font-weight: bold;
  font-display: swap;
}

@font-face {
  font-family: "Poppins";
  src: url("../assets/fonts/Poppins/Poppins-SemiBold.ttf");
  font-weight: 600;
  font-display: swap;
}

@font-face {
  font-family: "Poppins";
  src: url("../assets/fonts/Poppins/Poppins-LightItalic.ttf");
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}

:root {
  --accent-blue: #00b2ff;
  --accent-purple: #937af6;
  --dark-grey: #404040;
  --dark-bg: #1f1f1f;
  --light-grey: #c0c0c0;
}

html,
body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Poppins", sans-serif;
}

h1 {
  font-weight: normal;
  font-size: clamp(1.6rem, 4vw, 2.4rem);
  color: black;
}

h2 {
  font-weight: 300;
  font-style: italic;
  font-size: clamp(1.1rem, 2vw, 1.3rem);
}

h3 {
  font-size: clamp(1.2rem, 3vw, 2rem);
}

h3.center {
  padding: 0 min(22.4vw - 6rem, 16em);
}

h4 {
  font-size: clamp(1rem, 1.2vw, 1.2rem);
}

h1,
h4 {
  margin-block: 0;
}

h3,
h4 {
  font-weight: 600;
  color: var(--dark-grey);
}

h3.center,
h4.center {
  text-align: center;
}

h3.slide {
  font-size: clamp(1.6rem, 4vw, 2.4rem);
  font-weight: normal;
  margin-block: 0;
  color: black;
}

h3.slide b {
  font-weight: 600;
}

h2.list {
  margin-block: 0;
}

ul {
  list-style: none;
  padding-inline-start: 0;
  margin-block-start: 0;
  margin-inline-end: 0;
}

a {
  text-decoration: none;
}

a:hover {
  cursor: pointer;
}

a.navlinks {
  color: #000;
  font-weight: 600;
  transition: all 0.3s ease-in-out;
}

a.navlinks:hover {
  color: #fff;
}

a.navlinks:focus {
  color: var(--accent-purple);
}

.shrink a.navlinks {
  color: #fff;
}

.shrink a.navlinks:hover {
  color: var(--accent-blue);
}

.cta {
  margin-top: 2em;
}

button.btn {
  font-size: clamp(1rem, 2vw, 1.2rem);
  font-weight: 600;
  padding: 0.6em 2em;
  border-radius: 8px;
  color: #fff;
  border: none;
  cursor: pointer;
}

button.primary.btn {
  background-color: var(--accent-blue);
  transition: all 0.3s ease-in-out;
}

button.primary:hover {
  background-color: var(--accent-purple);
  transform: scale(1.2);
}

button.email-btn {
  background-color: black;
  padding: 1em;
  border-radius: 8px;
  border: none;
  cursor: pointer;
}

button.email-btn:hover {
  background-color: var(--accent-blue);
}

button.email-btn svg {
  fill: #fff;
  width: 18px;
  stroke: 3px;
  height: auto;
}

/*---------------------------------  Custom Element Styling  ----------------------------*/

input {
  font-family: "Poppins", sans-serif;
  font-size: 0.9rem;
  padding: 0.5em;
  border-radius: 4px;
  margin-bottom: 1rem;
}

input[type="button"],
input[type="submit"] {
  font-weight: 600;
  border-radius: 8px;
  padding: 0.5em 1em;
  background-color: var(--accent-blue);
  color: #fff;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

input[type="button"]:hover,
input[type="submit"]:hover {
  background-color: var(--accent-purple);
}

label {
  font-size: 0.8em;
  color: var(--light-grey);
  padding-bottom: 0.2em;
}

textarea {
  font-family: "Poppins", sans-serif;
  font-size: 0.9rem;
  padding: 0.4em;
  border-radius: 4px;
  height: 7.8rem;
}

/*---------------------------------  Layout Styling  ----------------------------*/

section,
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.boxed {
  width: min(85vw, 1200px);
}

.wide {
  width: min(90vw, 1600px);
}

.grid {
  display: grid;
  grid-template-columns: 1fr;
}

.stacked {
  width: 90vw;

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(120px, 100%), 1fr));
  gap: 1rem;
  justify-content: center;
}

.center {
  justify-items: center;
}

/*---------------------------------  Only for Laptop and Desktop Devices ----------------------------*/

@media only screen and (min-width: 1024px) {
  h2 {
    padding-right: 4rem;
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
</style>
