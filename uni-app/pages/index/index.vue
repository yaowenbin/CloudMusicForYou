<template>
	<div class="test-component"><hm-news-card :options="options" @click="onClick"></hm-news-card></div>
</template>

<script>
import HmNewsCard from '@/components/hm-news-card/index.vue';
export default {
	components: { HmNewsCard },
	data() {
		return {
			title: 'Hello',
			options: {
				img: '/static/hm-news-card/images/img_22726_0_0.png',
				title: '新闻标题',
				author: '作者',
				date: '16 MAY 2016',
				summary: '新闻概要。新闻概要长度最好控制在50字符以内',
				comments: '14 评论',
				likes: '254 喜欢',
				url: '',
				showComments: true,
				showLikes: true
			}
		};
	},
	onLoad() {},
	methods: {
		getComment:function(){
			const requestTask = uni.request({
			    url: 'https://www.example.com/request', //仅为示例，并非真实接口地址。
			    data: {
			        name: 'name',
			        age: 18
			    },
			    success: function(res) {
			        console.log(res.data);
			    }
			});
		},
		onClick: function(e) {
			console.log('onClick');
		}
	}
};
</script>

<style>
.content {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.logo {
	height: 200rpx;
	width: 200rpx;
	margin-top: 200rpx;
	margin-left: auto;
	margin-right: auto;
	margin-bottom: 50rpx;
}

.text-area {
	display: flex;
	justify-content: center;
}

.title {
	font-size: 36rpx;
	color: #8f8f94;
}
</style>
