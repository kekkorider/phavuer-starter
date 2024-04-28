<script setup>
import { Scene, Image, Body, useGame } from 'phavuer'

import { SCENES } from '../constants'

const game = useGame()
</script>

<template>
	<Scene :name="SCENES.MAIN">
		<Image
			:x="game.scale.width * 0.5"
			:y="game.scale.height * 0.5"
			:display-width="240"
			:display-height="72"
			texture="phavuer"
		>
			<Body
				:collideWorldBounds="true"
				:bounceX="0.4"
				:bounceY="0.4"
				:velocityX="175"
				:velocityY="-300"
				:dragX="10"
				:dragY="10"
			/>
		</Image>
	</Scene>
</template>
