<template>
<header class="header">
	<div class="header__content _container">
		<div class="header__menu menu">
			<div class="menu__icon icon-menu">
				<span></span>
				<span></span>
				<span></span>
			</div>
			<nav class="menu__body">
				<ul class="menu__list">
					<li><nuxt-link to="/news-social" class="menu__link">News & Social</nuxt-link></li>
					<li><nuxt-link to="/events" class="menu__link">Events</nuxt-link></li>
					<li><nuxt-link to="/rankings" class="menu__link">Rankings</nuxt-link></li>
					<li><nuxt-link to="/videos" class="menu__link">Videos</nuxt-link></li>
					<li><nuxt-link to="/gyms" class="menu__link">Gyms</nuxt-link></li>
					<li><nuxt-link to="/odds" class="menu__link">Odds</nuxt-link></li>
				</ul>
			</nav>
		</div>
	</div>
</header>
</template>

<style lang="scss">
.icon-menu {
	display: none;
	@media (max-width: 1200px) {
		display: block;
		position: absolute;
		top: 18px;
		right: 10px;
		width: 30px;
		height: 18px;
		cursor: pointer;
		z-index: 5;
		span {
			transition: all 0.3s ease 0s;
			top: calc(50% - 1px);
			left: 0px;
			position: absolute;
			width: 100%;
			height: 2px;
			background-color: #000;
			&:first-child {
				top: 0px;
			}
			&:last-child {
				top: auto;
				bottom: 0px;
			}
		}
		&._active {
			span {
				transform: scale(0);
				&:first-child {
					transform: rotate(-45deg);
					top: calc(50% - 1px);
				}
				&:last-child {
					transform: rotate(45deg);
					bottom: calc(50% - 1px);
				}
			}
		}
	}
}

</style>