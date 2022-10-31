<script lang="ts">
	import CopyPasswordField from '$lib/components/CopyPasswordField.svelte';
	import { t } from '$lib/translations';
	export let service: any;
</script>

<div class="flex space-x-1 py-5 font-bold">
	<div class="title">Directus</div>
</div>

<div class="grid grid-cols-2 items-center lg:px-10 px-2">
	<label for="adminEmail">Admin email</label>
	<input
			class="w-full"
			name="adminEmail"
			id="adminEmail"
			placeholder="user@example.com"
			value={service.directus.adminEmail}
	/>
</div>

<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="adminPassword">Admin password</label>
	<CopyPasswordField
			name="adminPassword"
			id="adminPassword"
			isPasswordField="true"
			value={service.directus.adminPassword}
	/>
</div>

<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="key">Key</label>
	<CopyPasswordField
			name="key"
			id="key"
			isPasswordField="true"
			value={service.directus.key}
			readonly
			disabled
	/>
</div>

<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="secret">Secret</label>
	<CopyPasswordField
			name="secret"
			id="secret"
			isPasswordField="true"
			value={service.directus.secret}
			readonly
			disabled
	/>
</div>

<div class="flex space-x-1 py-5 font-bold">
	<div class="title">PostgreSQL</div>
</div>

<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="postgresqlHost">PostgreSQL Host</label>
	<CopyPasswordField
		name="postgresqlHost"
		id="postgresqlHost"
		value={service.directus.postgresqlHost}
		readonly
		disabled
	/>
</div>
<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="postgresqlPort">PostgreSQL Port</label>
	<CopyPasswordField
		name="postgresqlPort"
		id="postgresqlPort"
		value={service.directus.postgresqlPort}
		readonly
		disabled
	/>
</div>
<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="postgresqlUser">PostgreSQL User</label>
	<CopyPasswordField
		name="postgresqlUser"
		id="postgresqlUser"
		value={service.directus.postgresqlUser}
		readonly
		disabled
	/>
</div>
<div class="grid grid-cols-2 items-center lg:px-10">
	<label class="text-base font-bold text-stone-100" for="postgresqlPassword">PostgreSQL Password</label>
	<CopyPasswordField
		name="postgresqlPassword"
		id="postgresqlPassword"
		isPasswordField
		value={service.directus.postgresqlPassword}
		readonly
		disabled
	/>
</div>
