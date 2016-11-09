<!-- DetailHeader.vue -->
<template>
	<header class="header">
		<div class="header_inner flexWrap">
			<div 
				id="header_btn_nav" 
				class="header_btn header_btn_back"
				v-on:click="goBack"
				>返回</div>
			<div class="header_cont flex">详情</div>
			<div class="header_btn header_btn_cart"></div>
		</div>
	</header>
</template>

<style>
	.flexWrap {
		display: -webkit-flex;
		display: flex;
	}
	.flex {
		flex: 1;
	}
	.header {
		height: 0.88rem;
	}
	.header_inner {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 99;
		max-width: 640px;
		height: 0.88rem;
		box-sizing: border-box;
		margin: 0 auto;
		padding: 0 0.24rem;
		border-bottom: 0.02rem solid #80ccd6;
		background-color: #fff;
	}
	.header_btn {
		width: 0.5rem;
		height: 100%;
		background-repeat: no-repeat;
	}
	.header_btn_back {
		line-height: 0.86rem;
	}
	.header_cont {
		text-align: center;
		padding: 0 0.4rem;
		line-height: 0.86rem;
		font-size: 15px;
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}
	.header_btn:active {
		opacity: 0.7;
	}
</style>
<script>
	export default {
		methods: {
			goBack(){
				window.history.back();
			}
		}
	}
</script>