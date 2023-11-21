<script>
	import Container from '$lib/components/Day2/Container.svelte';
	import profile from '$lib/assets/profile-unsplash.jpg';
	import Lock from '$lib/components/icons/Lock.svelte';
	import Hide from '$lib/components/icons/Hide.svelte';
	import Switch from '$lib/components/General/Switch.svelte';
</script>

<Container color={'#f6f7f8'}>
	<!-- title  -->
	<h1>Enter your password</h1>

	<!-- profile -->
	<div>
		<div
			class="h-[72px] w-[72px] rounded-full bg-cover"
			style="background-image: url({profile});"
		></div>
		<p>Business Accountant</p>
		<h3>Sarah Bills</h3>
	</div>

	<!-- inputs-->
	<div>
		<h4>Password</h4>
		<div>
			<div>
				<Lock />
			</div>
			<input type="password" />

			<div>
				<Hide />
			</div>
		</div>
		<div>
			<div>
				<Switch />
				<span>Stay signed in</span>
			</div>
			<button>Continue</button>
		</div>
	</div>

	<!-- reset password  -->
	<button>Reset password</button>
</Container>
