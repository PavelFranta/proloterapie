<!-- <script>
	import { createForm } from 'svelte-forms-lib';
	import * as yup from 'yup';

	let y;

	const { form, errors, handleChange, handleSubmit } = createForm({
		initialValues: {
			name: '',
			email: ''
		},
		validationSchema: yup.object().shape({
			name: yup.string().required(),
			email: yup.string().email().required(),
			tel: yup.string().required(),
			problemDescription: yup.string().required()
		}),
		onSubmit: (values) => {
			alert(JSON.stringify(values));
		}
	});
</script>

<svelte:window bind:innerWidth={y} />
<form on:submit={handleSubmit} class="text-black pt-12 px-6 pb-6">
	<div class="flex flex-col md:flex-row md:justify-center">
		<div class="flex flex-col md:mr-9">
			<label for="name">Jméno a příjmení</label>
			<input
				class="text-lg"
				id="name"
				name="name"
				on:change={handleChange}
				on:blur={handleChange}
				bind:value={$form.name}
			/>
			{#if $errors.name}
				<small>Vyplňte prosím jak Vás máme oslovovat</small>
			{/if}

			<label for="email">Email</label>
			<input
				class="text-lg"
				id="email"
				name="email"
				on:change={handleChange}
				on:blur={handleChange}
				bind:value={$form.email}
			/>
			{#if $errors.email}
				<small>Vyplňte prosím kam Vám můžeme napsat</small>
			{/if}

			<label for="tel">Telefonní číslo</label>
			<input
				class="text-lg"
				id="tel"
				name="tel"
				on:change={handleChange}
				on:blur={handleChange}
				bind:value={$form.tel}
			/>
			{#if $errors.tel}
				<small>Vyplňte prosím telefonní číslo pro snadnější komunikaci</small>
			{/if}
		</div>
		<div class="flex flex-col">
			<label for="tel">Stručně nám popiště co Vás trápí</label>
			<textarea
				class="text-lg"
				rows={y < 768 ? 4 : 6}
				id="problemDescription"
				name="problemDescription"
				on:change={handleChange}
				on:blur={handleChange}
				bind:value={$form.problemDescription}
			/>
			{#if $errors.problemDescription}
				<small>Popište nám prosím v krátkosti jaký problém si přejete řešit</small>
			{/if}
		</div>
	</div>
	<button type="submit" class="bg-white md:block md:m-auto text-black w-full rounded-md p-4 mb-6 md:w-56"
		>ODESLAT</button
	>
</form>

<style>
	textarea,
	form input {
		@apply rounded-md mt-1 p-1 mb-1.5;
	}

	textarea {
		@apply mb-6;
	}
	small,
	label {
		@apply text-white;
	}
</style> -->
