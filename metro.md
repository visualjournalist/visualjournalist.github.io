---
layout: default
title: Panoramic drawing of a metro train
permalink: metro
image: sketchbook/metro.jpg
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
		<img class="vj__pano__image" src="/img/panoramic-metro.jpg" alt="A panoramic illustration of a metro train twisting across a city. By Brian Williamson." style="">
	</div>

	<div id="swipe" class="vj__pano__swipe-button">Swipe to explore <span class="hideMobile">this panoramic image</span></div>


	<div class="vj__section__full-width" style="padding-top: 30px;">
		<div class="vj__grid__full">
			<div class="vj__grid">
				<div class="vj__story">
					
					<h1 class="vj__title">An accordion-fold, panoramic train ride</h1>
					<p><strong>This is a single drawing that continues across city streets, underground and over bridges.</strong></p>

					<p>It's a tortoise and the hare race between friends. One friend cruises and weaves through traffic in a car. The other transfers between buses and subways, riding up and down escalators. Their paths braid and fork over bridges and through tunnels on their way to a shared destination across town.</p>

					<p>As a printed book, it would be an accordion fold mural, drawn across 50 feet of paper. The digital edition spans 150,000 pixels. Each page turn (or swipe of the screen) creates dynamic movement and reveals visual surprises: The ceiling in one spread becomes the sidewalk in the next; train tracks converge to form power lines as the perspective is smashed and inverted.</p>
				</div>
			</div>
		</div>
	</div>
</article>
