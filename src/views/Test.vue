<template>
  <div class="test">
    <p class="test__text">
      test text
    </p>
    <button @click="changeArr">配列変えます！！！</button>
    <div>{{ testData }}</div>
    <div v-if="isTestData">
      <div
        v-for="(item, index) in testData"
        :key="index">
        {{ item }}
      </div>
    </div>
    <div v-else>
      <div
        v-for="(item, index) in testData2"
        :key="index">
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'TestPage',
  data () {
    return {
      testData: [1, 2],
      testData2: [5, 4],
      isTestData: true,
      test: []
    }
  },
  components: {
  },
  methods: {
    changeArr () {
      this.isTestData = !this.isTestData
    }
  }
}
</script>

<style scoped lang="scss">
.test {
  .test__text {
    color: red;
  }
}
</style>
