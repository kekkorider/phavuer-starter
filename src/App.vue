<script setup>
import { Game } from 'phavuer'

import PreloadScene from './scenes/Preload.vue'
import MainScene from './scenes/Main.vue'

const config = {
	width: 600,
	height: 300,
	backgroundColor: 0x181818,
	gameTitle: 'Phavuer Starter',
	gameVersion: '0.1.0',
	transparent: false,
	scale: {
		mode: Phaser.Scale.FIT,
		autoCenter: Phaser.Scale.CENTER_BOTH,
	},
	physics: {
		default: 'arcade',
		arcade: {
			gravity: { y: 200 },
			debug: true,
		},
	},
}
</script>

<template>
	<Game :config="config">
		<PreloadScene :autoStart="true" />
		<MainScene :autoStart="false" />
	</Game>
</template>
