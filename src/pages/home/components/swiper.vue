<template>
<div class="wrapper">
	<swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
    	<img class="swiper-img" :src="item.imgUrl" />    	
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
	name: 'HomeSwiper',
	data () {
		return {
			swiperOption: {
				pagination: '.swiper-pagination',
				loop: true
			},
			swiperList:[{
				id: '0001',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/6b6fd3d9e40b749ac1d189ce80ebb3cc.jpg_750x200_9616e2e7.jpg'
			},{
				id: '0002',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/942d87cc1576c333c77dc1f86af145cd.jpg_750x200_d25bf3eb.jpg'
			},{
				id: '0003',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e5104d77fbfdb522bd4fe4f0451e517f.jpg_750x200_7d44f64b.jpg'
			},{
				id: '0004',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/5aed0c962f09f0681d31c6e7a159a80d.jpg_750x200_5929f4c9.jpg'
			}]
		}
	}
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
	background: #fff
.wrapper
	background: #eee
	overflow: hidden
	width: 100%
	height: 0
	padding-bottom: 27%	
	.swiper-img
		width: 100%
</style>