<script setup lang="ts">
import { ipcRenderer } from 'electron'

function minimizeWindow() {
	ipcRenderer.send('window-min', '')
}

function maximizeWindow() {
	ipcRenderer.send('window-max', '')
}

function closeWindow() {
	ipcRenderer.send('window-close', '')
}
</script>

<template>
	<div id="titlebar">
		<span id="title">NOUMENON</span>
		<span class="title-button" id="minimize" @click="minimizeWindow">
			<img :src="'./icons/min.svg'" />
		</span>
		<span class="title-button" id="maximize" @click="maximizeWindow">
			<img :src="'./icons/max.svg'" />
		</span>
		<span class="title-button" id="close" @click="closeWindow">
			<img :src="'./icons/close2.svg'" />
		</span>
	</div>
</template>

<style scoped>
#titlebar {
	width: 100%;
	height: 24px;
	background-color: #262626;
	position: fixed;
	top: 0px;
	left: 0px;
	-webkit-app-region: drag;
}

#title {
	font-family: Aleo-Bold;
	color: #935C4D;
	font-size: 16px;
	position: absolute;
	margin: 0;
	top: 50%;
	left: 8px;
	vertical-align: middle;
	transform: translate(0, -50%) translate(0, 2px);
	user-select: none;
}

.title-button {
	position: absolute;
	top: 0px;
	padding: 0 8px;
	height: 24px;
	-webkit-app-region: no-drag;
}

.title-button > img {
	position: relative;
	filter: invert(100%) sepia(0%) saturate(7397%) hue-rotate(271deg) brightness(122%) contrast(73%);
}

.title-button:hover {
	cursor: pointer;
}

#minimize > img, #maximize > img {
	top: 2px;
}

#close:hover {
	background-color: red;
}

#close:hover > img {
	filter: invert(100%) sepia(1%) saturate(202%) hue-rotate(239deg) brightness(118%) contrast(100%);
}

#maximize:hover, #minimize:hover {
	background-color: #484848;
}

#maximize {
	right: 40px;
}

#minimize {
	right: 80px;
}

#close {
	right: 0px;
}
</style>