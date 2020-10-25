<script lang="ts">
	import { methods } from "@sidetree/wallet";
	let mnemonic;
	let profile;
	methods.toMnemonic("test").then(x => {
		mnemonic = x;
		return methods.toDidDocForProfile(x.value, 0, "sidetree");
	}).then(x => profile = x);

</script>

<main>
	<h1>Hello world!</h1>
	<p>{JSON.stringify(mnemonic)}</p>
	<p>{JSON.stringify(profile)}</p>
</main>
