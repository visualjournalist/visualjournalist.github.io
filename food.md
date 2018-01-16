---
layout: default
title: Panoramic drawing of food in St. Louis
permalink: food
image: sketchbook/food.jpg
exclude_from_nav: true
excerpt: A single drawing that continues across city streets,underground and over bridges.
---

<style type="text/css">

	.vj__project .vj__pano {
		box-shadow: inset 0 0 5px #333;
		height: 300px;
		margin-top: 62px; 
		overflow-x: auto;
		overflow-y: hidden;
		position: relative;
		width: 100%;
	}
	.vj__project img.vj__pano__image {
		height: 300px;
		margin: 0;
		padding: 0;
		width: auto;
	}
	.vj__pano__swipe-button {
		background: rgba(210,10,10,0.9) url(/img/fpo__icon-tap.png) no-repeat center left / 40px 40px;
		border-radius: 0 20px 20px 0;
		color: #FFF;
		cursor: pointer;
		display: inline-block;
		height: 20px;
		padding: 5px 15px 25px 48px;
		position: absolute;
			top: 350px;
		width: auto;
		z-index: 9998;
	}
</style>

<script type="text/javascript">

		/*
		function scrollPano(){
			var imageWidthTest = $("#illustration img").width();

			var percent = 0.31
			var scrollPercentage = imageWidthTest * percent;

			$('#illustration').animate({scrollLeft: scrollPercentage}, 1000);
		}
		*/
		var scrollStart = 0.31

		function scrollPano(scrollPercentageNumber){
			var imageWidthTest = $("#illustration img").width();

			var percent = scrollPercentageNumber;
			var scrollPercentage = imageWidthTest * percent;

			$('#illustration').animate({scrollLeft: scrollPercentage}, 1500);
		}

		$(window).on('load', function() {
			scrollPano(scrollStart);

			$('#swipe').click(function(){
				var randomPercent = Math.random();
				scrollPano(randomPercent);
			})

		});

</script>

<article class="post">
	<div id="illustration" class="vj__pano">
		<img class="vj__pano__image" src="/img/pano_food.jpg" alt="A panoramic illustration of food in St. Louis. By Brian Williamson." style="">
	</div>

	<div id="swipe" class="vj__pano__swipe-button">Swipe to explore <span class="hideMobile">this panoramic image</span></div>


	<div class="vj__section__full-width" style="padding-top: 30px;">
		<div class="vj__grid__full">
			<div class="vj__grid">
				<div class="vj__story">
					
					<h1 class="vj__title">An accordion-fold, panoramic look at food</h1>

					<p>I created this simple 8-foot long, accordion fold drawing about food in St. Louis for FoodStock, a 2011 exhibition at Mad Art Gallery.</p>

					<p>You can scroll across the entire panoramic illustration, from backyard barbecues to food trucks to fine dining and bars. I wanted to create an image that worked for individual pages, spreads and also when it was unfolded to different lengths.</p>

					<img src="/img/pano_food_photo_book.jpg" alt="Photo of the accordion-fold book." style="max-width: 640px; margin: 20px auto; display: block;" />

					<p>I started off experimenting with gouache and a limited color palette. But eventually I decided to draw the line art scenes directly in a Moleskine Japanese album. Rather than sticking with one perspective system for the entire image, I varied and twisted the perspective between spreads.</p>
				</div>
			</div>
		</div>
	</div>
</article>
