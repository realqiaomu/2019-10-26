<template>
	<view class="content">
		<view :class="starClass" @click="star"></view>
	</view>
</template>

<script>
/* 	import { uniIcons } from '@dcloudio/uni-ui'; */
	export default {
		data() {
			return {
				starClass:'fave',
			}
		},
		methods: {
			star(){
				this.starClass += ' active';
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
	.fave {
		background: url(../../static/twitter_fave.png) no-repeat;
		background-position: 0 0;
		width: 70px;
		height: 50px;
		cursor: pointer;
	}
	.fave.active{
		background-position: -3519px 0;
		transition: background 1s linear/* steps(50) */;
	}
</style>
