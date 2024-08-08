<template>
  <div class="header">
    <div class="box home" @click="to('/')">
      <p class="mdi mdi-home icon"></p>
      Home
    </div>
    <div class="box events">
      <p class="mdi mdi-calendar icon"></p>
      Events
    </div>
    <div class="box aboutus">
      <p class="mdi mdi-help icon"></p>
      About Us
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    to(page) {
      this.$router.push({ path: page });
    },
  },
};
</script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  font-family: Arial;
  height: 80px;
  display: flex;

  justify-content: center;
  align-items: center;

  box-shadow: 0 0px 10px rgba(0, 0, 0, 0.1);
}

.icon {
  font-size: 30px;
  padding: 10px;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 33%;
  height: 80px;
  font-size: 15px;
  border-left: solid 0.5px;
  border-right: solid 0.5px;
  font-weight: 600;
}

.box:hover {
  width: 50%;
  transition: width 1s ease;
  background-color: #fafafa;
}
</style>
