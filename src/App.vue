<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import SideBar from './components/SideBar.vue'
import TitleBar from './components/TitleBar.vue'
</script>

<template>
	<TitleBar />
	<SideBar />
</template>

<style>
@font-face {
	font-family: Aleo-Regular;
	src: url(./fonts/Aleo-Regular.ttf);
}

@font-face {
	font-family: Aleo-Bold;
	src: url(./fonts/Aleo-Bold.ttf);
}

#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-left: 80px;
}

.logo-box {
	display: flex;
	width: 100%;
	justify-content: center;
}

.static-public {
	display: flex;
	align-items: center;
	justify-content: center;
}

.static-public code {
	background-color: #eee;
	padding: 2px 4px;
	margin: 0 4px;
	border-radius: 4px;
	color: #304455;
}
</style>
