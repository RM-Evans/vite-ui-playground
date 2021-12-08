<script setup lang="ts">
import { ref } from "vue"

defineProps<{ msg: string }>()

const count = ref(0)

const tabs = [
	{ label: "first", name: "first" },
	{ label: "second", name: "second" },
]
</script>

<template>
	<el-scrollbar>
		<el-container class="main-con">
			<h1>{{ msg }}</h1>

			<el-header>
				<el-button class="btn" color="#ff4a9d" plain>just button</el-button>
			</el-header>
			<el-tabs>
				<el-tab-pane v-for="tab in tabs"></el-tab-pane>
			</el-tabs>
			<!-- label - name -->
			<el-aside></el-aside>
		</el-container>
	</el-scrollbar>
</template>

<style scoped>
.main-con {
	background-color: #4c5257;
}
/* .btn {
	outline: solid #c4c4c4 2px;
	border-radius: 100px;
} */
a {
	color: #42b983;
}
h1 {
	color: #c4c4c4;
}

label {
	margin: 0 0.5em;
	font-weight: bold;
}

code {
	background-color: #eee;
	padding: 2px 4px;
	border-radius: 4px;
	color: #304455;
}
</style>
