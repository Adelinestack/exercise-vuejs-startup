<template>
  <BgContainer :bgcolor="bgColor">
    <p>{{bgColor}}</p>
  </BgContainer>
</template>

<script>
import styled from "vue-styled-components";

const BgContainer = styled("div", { bgcolor: String })`
  background-color: ${props => props.bgcolor};
  height: 200px;
`;

export default {
  name: "BgModifier",
  data: () => ({
    bgColor: "white"
  }),
  components: {
    BgContainer
  },

  created() {
    setInterval(() => {
      return this.bgColor === "white"
        ? (this.bgColor = "green")
        : (this.bgColor = "white");
    }, 2000);
  }
};
</script>



