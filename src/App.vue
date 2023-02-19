<template>
	<div class="container">
		<div  >
			<TabsComp :tabs="tabs" />

		</div>
	</div>
</template>

<script>
import TabsComp from "./components/TabsComp.vue";
export default {
	name: "App",
	components: {
		TabsComp,
	},
	data() {
		return {
      showBodyTitle:'',
			tabs: [
				{
					title: "Info",
					body: "Info: Design the following tabs component using HTML, CSS, and vanilla JavaScript",
				},
				{ title: "Phone", body: "Phone: 07889883474" },
				{ title: "Email", body: "EmailL: murtajaadnan@gmail.com" },
				{ title: "Github", body: "Github: https://murtaja@github" },
				{ title: "LinkedIn", body: "LinkedIn: https://murtaja@LinkedIn" },
			],
		};
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}

</style>
