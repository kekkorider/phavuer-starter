<script setup>
import { Scene } from 'phavuer'

import { SCENES } from '../constants'
import assets from '../assets.json'

function onPreload(scene) {
	Object.keys(assets).forEach(methodName => {
		assets[methodName].forEach(args => scene.load[methodName](...args))
	})
}

function onCreate(scene) {
	scene.scene.start(SCENES.MAIN)
	scene.scene.stop(SCENES.PRELOAD)
}
</script>

<template>
	<Scene :name="SCENES.PRELOAD" @preload="onPreload" @create="onCreate" />
</template>
