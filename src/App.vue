<template>
	<div id="app">

		<md-whiteframe md-tag="md-toolbar" md-elevation="2" md-theme="black" class="md-primary">

			<router-link tag="md-button" v-bind:to="{ name: 'login' }" class="md-icon-button">
				<md-icon>home</md-icon>
			</router-link>

			<h2 class="md-title" style="flex: 1">Demo API</h2>
			<navegation></navegation>
		</md-whiteframe>

		<router-view></router-view>

		<md-dialog-alert
		  :md-title="alert.title"
		  :md-content-html="alert.content"
		  ref="dialog">
		</md-dialog-alert>

	</div>
</template>

<script>
	import Navegation from './components/style/navegation.vue'
	import { util } from './utils/util.js'
	export default {
		components: {
			navegation: Navegation
		},
		data() {
			return {
				alert: util.custom_alert.alert
			}
		}
	}
</script>

<style>
	body {
		background: #ECEFF1;
	}
	.container {
		width: 70%;
		margin: 30px auto;
	}
	.left-padding {
		padding-left: 10px;
	}
	.right-padding {
		padding-right: 10px;
	}
	.md-card .md-card-header {
		padding: 10px 16px 5px 16px;
	}
	.md-card .md-display-1 {
		font-weight: 500;
	}
	.md-table .md-table-cell .md-button:last-child {
    margin: 6px 0px 6px 8px;
	}
	.md-toolbar .md-title {
    font-weight: 500;
	}
	.if-div {
		display: flex;
		height: 100%;
		align-items: center;
	}
	.md-spinner {
		margin: 0 auto;
	}
</style>
