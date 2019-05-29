<template>
  <BgButtonContainer :bgcolor="bgColor">
    <button @click="changeColor">Change color</button>
    <p>{{bgColor}}</p>
  </BgButtonContainer>
</template>

<script>
import styled from "vue-styled-components";

const BgButtonContainer = styled("div", { bgcolor: String })`
  background-color: ${props => props.bgcolor};
  height: 200px;
`;

export default {
  name: "BgButtonModifier",
  data: () => ({
    bgColors: ["blue", "purple", "yellow", "salmon"],
    bgColor: "blue"
  }),
  components: {
    BgButtonContainer
  },
  methods: {
    changeColor() {
      this.bgColor = this.bgColors[Math.floor(Math.random() * 4)];
    }
  }
};
</script>