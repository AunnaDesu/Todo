<template>
  <div>
    <YO @Input="validate"></YO>
    <Lo :A1="A1"></Lo>
    </div>
</template>

<script>
import YO from "../components/YO.vue"
import Lo from "../components/Lo.vue"
export default {
  data: () => ({
    A1: [],
  }),
components :{YO,Lo},
A1: "Input",
  methods: {
    validate(select, name) {
      this.A1.push({
        name: select + " : " + name,
      });
    },
  },
};
</script>

<style>

</style>