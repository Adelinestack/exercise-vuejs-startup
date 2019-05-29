<template>
  <BgButtonsContainer :bgcolor="bgColor">
    <button @click="changeColor('blue')">Change color</button>
    <button @click="changeColor('pink')">Change color</button>
    <button @click="changeColor('yellow')">Change color</button>
    <button @click="changeColor('red')">Change color</button>
    <p>{{bgColor}}</p>
  </BgButtonsContainer>
</template>

<script>
import styled from "vue-styled-components";

const BgButtonsContainer = styled("div", { bgcolor: String })`
  background-color: ${props => props.bgcolor};
  height: 200px;
`;

export default {
  name: "BgButtonsModifier",
  data: () => ({
    bgColor: "blue"
  }),
  components: {
    BgButtonsContainer
  },
  methods: {
    changeColor(color) {
      this.bgColor = color;
    }
  }
};
</script>