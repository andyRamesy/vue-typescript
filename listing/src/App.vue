<template>
	<div>
		<p>{{ jobs[0].title }} -</p>
		<!-- <button @click="changeName('qsdf')">change name</button>
		<button @click="changeAge(30)">change age</button> -->
	</div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from "vue";
import Job from "./types/Job";
// import { reactive, ref } from 'vue';

// let name = "Andy"
export default defineComponent({
	name: "App",
	components: {},
	setup() {
		// const state = reactive({
		// 	name: "Andy",
		// 	age: 25 as number | string
		// });
		// state.name = "Mo";
		// state.age = 999
		// return { ...toRefs(state) };
		// const name = ref("link");
		// const age = ref<number | string>(25);
		// name.value = "yoshi";
		// name.value = "XY";
		// return { name, age };
    const jobs = ref<Job[]>([
      {
        title: "Farmer", location: "io io branch", salary: 1000, id: "1"
      },
      {
        title: "Roller", location: "tex", salary: 3000, id: "2"
      },
      {
        title: "Seller", location: "cinq quatre", salary: 250, id: "3"
      },
      {
        title: "colter", location: "bunnch", salary: 4000, id: "4"
      },
      {
        title: "actor", location: "xyz", salary: 23, id: "5"
      },
    ])
    return {jobs}
	}
});
</script>

<style></style>
