<script lang="ts">
	import { onMount } from 'svelte';
	import avatar from '$lib/assets/avatar.jpg';

	const TIMEZONE = 'Asia/Bangkok';

	let time = $state('');

	function formatTime(date: Date) {
		return new Intl.DateTimeFormat('en-GB', {
			timeZone: TIMEZONE,
			hour: '2-digit',
			minute: '2-digit',
			hour12: false
		}).format(date);
	}

	onMount(() => {
		const tick = () => {
			time = formatTime(new Date());
		};

		tick();
		const id = setInterval(tick, 1000);
		return () => clearInterval(id);
	});
</script>

<main class="wrapper">
	<header class="intro">
		<img class="avatar" src={avatar} alt="Pat" width="88" height="88" />
		<p class="eyebrow">
			Chayapat Pakham · Thailand{#if time}
				{' · '}<span class="local-time" data-tooltip={TIMEZONE}>{time}</span>{/if}
		</p>
		<h1>Hi, I'm Pat</h1>
		<p class="bio">
			I'm a <strong>web developer</strong>, artist and student who likes making things that feel
			fun to use. Started in game dev, wandered through Machine Learning and apps, and landed on
			the web, where I've stayed
		</p>
	</header>

	<section class="section" aria-labelledby="contact-heading">
		<h2 id="contact-heading">Say hi</h2>
		<ul class="links">
			<li>
				<a href="mailto:pathonscript@gmail.com">email</a>
			</li>
			<li>
				<a href="https://github.com/PatatoBit" target="_blank" rel="noopener">github</a>
			</li>
			<li>
				<a href="https://twitter.com/patatobit" target="_blank" rel="noopener">twitter</a>
			</li>
			<li>
				<a href="https://www.linkedin.com/in/patato/" target="_blank" rel="noopener">linkedin</a>
			</li>
		</ul>
	</section>
</main>
