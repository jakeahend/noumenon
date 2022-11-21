<template>
	<div id="sidebar">
		<span class="sidebar-button" id="characters">
			<img :src="'./icons/characters.svg'" />
		</span>
		<span class="sidebar-button" id="campaigns">
			<img :src="'./icons/campaigns.svg'" />
		</span>
	</div>
</template>

<style>
#sidebar {
	height: 100%;
	width: 60px;
	position: fixed;
	z-index: 1;
	top: 24px;
	left: 0;
	background-color: #262626;
	overflow-x: hidden;
	padding-top: 4px;
}

.sidebar-button {
	position: relative;
}

.sidebar-button > img {
	filter: invert(100%) sepia(0%) saturate(7397%) hue-rotate(271deg) brightness(122%) contrast(73%);
}

.sidebar-button:hover {
	cursor: pointer;
}

.sidebar-button:hover > img {
	filter: invert(44%) sepia(5%) saturate(4507%) hue-rotate(326deg) brightness(83%) contrast(76%);
}
</style>