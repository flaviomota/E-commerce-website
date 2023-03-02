<template>
	<div class="banner">
		<div class="container">
			<div class="banner-content">
				
				<div class="main-banner">
					<div class="img-container">
						<img src="@/assets/images/banner1.jpg"  alt=""/>
						<div class="img-content">
							<span>
								Banner
							</span>
							<h3>Your Title Text</h3>
						</div>
					</div>
				</div>
				
				<div class="category-banner">
					<div class="top">
						<div class="img-container">
							<img src="@/assets/images/banner2.jpg"  alt=""/>
							<div class="img-content">
								<h3>Women</h3>
							</div>
						</div>
						<div class="img-container">
							<img src="@/assets/images/banner3.png"  alt=""/>
							<div class="img-content">
								<h3>Men</h3>
							</div>
						</div>
					</div>
					<div class="bottom">
						<div class="img-container">
							<img src="@/assets/images/banner4.png"  alt=""/>
							<div class="img-content">
								<h3>Accessories</h3>
							</div>
						</div>
					</div>
				</div>

			</div>

			<div class="banner-services">
				<div v-for="n in 3" :key="n" class="service">
					<span class="icon">
						<img src="@/assets/images/delivery-truck.png" alt="" />
					</span>
					<div class="details">
						<h6>FREE SHIPPING</h6>
						<p>On all UA order or order above €100</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup>

</script>

<style scoped>
img {
	height: 100%;
}

.banner {
	border-bottom: 2px solid #F8F8F8;
	margin-bottom: 100px;
}

.banner .container {
	max-width: calc(1440px - 170px);
	width: 100%;
	margin: auto;
}

.banner-content {
	display: flex;
	justify-content: space-between;
	padding: 40px 0;
}

.banner-content > div {
	flex: 0 0 calc(50% - 20px);
	max-width: calc(50% - 20px);
	width: 100%;
}

.img-container {
	position: relative;
	height: 100%;
	width: 100%;
}

.img-container img {
	width: 100%;
	object-fit: cover;
}
.img-container .img-content {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	background-color: #FFFFFF;
	border-radius: 4px;
	padding: 16px 32px;
	text-align: center;
}

.img-content span {
	font-weight: 600;
	font-size: 12px;
	line-height: 13px;
	color: #121212;
	opacity: 0.4;
	text-transform: uppercase;
}

.img-content h3 {
	font-weight: 600;
	font-size: 22px;
	line-height: 25px;
	color: #121212;
	text-transform: uppercase;
	margin-top: 5px;
}

.category-banner .top {
	display: flex;
	justify-content: space-between;
	margin-bottom: 30px;
}

.category-banner .top > div {
	flex: 0 0 calc(50% - 20px);
	max-width: calc(50% - 20px);
	width: 100%;
}

.banner-services {
	display: flex;
	justify-content: space-between;
	margin-bottom: 30px;
	align-items: center;
}

.banner-services > div {
	flex: 0 0 calc(33.33% - 20px);
	max-width: calc(33.33% - 20px);
	width: 100%;
	display: flex;
	align-items: center;
}

.service .details {
	margin-left: 10px;
}

.details h6 {
	font-weight: 500;
	font-size: 12px;
	line-height: 22px;
}

.details p {
	font-weight: 500;
	font-size: 12px;
	line-height: 22px;
	opacity: 0.9;
}
</style>