<template>
	<div>
		<div class="container">
			
			<div class="category-header">
				<h3>WOMEN's</h3>
				
				<div class="tabs">
					<div
						v-for="(tab, i) in tabs" :key="tab"
						class="tab"
						@click="activeIndex = i"
						:class="{'active': activeIndex === i}"
					>
						{{ tab }}
					</div>
				</div>

			</div>

				<div class="products">
					<div v-for="n in 6" :key="n" class="single-product">
						<div class="img-container">
							
							<img src="@/assets/images/p1.jpg" alt="" />

							<div class="sale">
								-50%
							</div>

						</div>
						<div class="product-content">
							<h6 class="name">
								Short Sleeved Hoodie
							</h6>
							<div class="rating">
								<span class="price">
									€ 32.00
								</span>
								<span class="icon">
									<img src="@/assets/images/rating.png" alt="" />
								</span>
							</div>
						</div>
					</div>
				</div>

				<button class="btn">
					SEE ALL
				</button>

		</div>
	</div>
</template>

<script setup>
import { ref } from 'vue';

const tabs = ref([
	'NEW ARRIVALS',
	'SPECIALS',
	'BESTSELLERS',
	'MOST VIEWED',
	'FEATURED PRODUCTS'
]);

const activeIndex = ref(0);
</script>

<style scoped>
.category-header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 50px;
}

.category-header h3 {
	font-style: normal;
	font-size: 22px;
	font-weight: 600;
	line-height: 25px;
}

.tabs {
	display: flex;
	align-items: center;
}

.tabs .tab {
	font-weight: 600;
	font-size: 12px;
	line-height: 13px;
	opacity: 0.6;
	transition: 0.3s;
	margin-right: 32px;
	cursor: pointer;
}

.tabs .tab.active,
.tabs .tab:hover {
	opacity: 1;
}

.products {
	display: grid;
	grid-template-columns: 1fr 1fr 1fr 1fr;
	gap: 30px;
}

.single-product .product-content {
	padding: 10px 0px;	
}

.single-product .product-content h6 {
	font-weight: 400;
	font-size: 14px;
	line-height: 16px;
	opacity: 0.6;
}

.single-product .product-content .rating {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-top: 5px;
}

.single-product .rating .price {
	font-weight: 700;
	font-size: 14px;
	line-height: 16px;
}

.single-product .img-container {
	position: relative;
}

.single-product .img-container .sale {
	position: absolute;
	top: 0;
	left: 0;
	padding: 9px;
	background: #E91E63;
	right: auto;
	font-weight: 700;
	font-size: 12px;
	line-height: 13px;
	text-align: center;
	color: #FFFFFF;
}
</style>