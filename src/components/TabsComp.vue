<template lang="">
	<div class="container">
		<div
			:key="tab.title"
			v-for="(tab, index) in tabs"
			@click="handleClick(index)"
		>
			<span class="tab" :class="[index == id ? 'selected' : '', 'tab']">{{
				tab.title
			}}</span>
			<span v-show="index != 4" class="divider"></span>
		</div>
	</div>
	<body class="textBody">
		{{ tabs[id].body }}
	</body>
</template>
<script>
export default {
	name: "TabsComp",
	props: {
		tabs: Array,
	},
	data() {
		return {
			id: 0,
		};
	},
	methods: {
		handleClick(id) {
			this.id = id;
		},
	},
};
</script>
<style lang="css" scoped>
.container {
	display: flex;
	align-items: center;
	justify-content: center;
	padding-left: 100px;
}
.tab {
	padding: 15px;
	border-bottom: solid black 2px;
	display: inline-block;
	cursor: pointer;
}
.divider {
	border-left: 2px solid black;
	height: 500px;
}
.selected {
	background: blue;
	color: white;
}
.textBody {
	margin-top: 30px;
}
</style>
