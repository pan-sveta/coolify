<script lang="ts">
	import CopyPasswordField from '$lib/components/CopyPasswordField.svelte';
	import { t } from '$lib/translations';
	export let service: any;
</script>

<div class="flex space-x-1 py-5 font-bold">
	<div class="title">Hasura</div>
</div>

<div class="grid grid-cols-2 items-center lg:px-10 px-2">
	<label for="graphQLAdminPassword">GraphQL Admin Password</label>
	<CopyPasswordField
		name="graphQLAdminPassword"
		id="graphQLAdminPassword"
		isPasswordField
		value={service.hasura.graphQLAdminPassword}
		readonly
		disabled
	/>
</div>
<div class="lg:px-10 px-2 py-4">Hasura Console is <span class="text-warning">not enabled by default</span> for security reasons. <br>To enable it, add the following secret:<br><br> <code>HASURA_GRAPHQL_ENABLE_CONSOLE=true</code></div>

<div class="flex space-x-1 py-5 font-bold">
	<div class="title">PostgreSQL</div>
</div>

<div class="space-y-2">
	<div class="grid grid-cols-2 items-center lg:px-10 px-2">
		<label for="postgresqlUser">{$t('forms.username')}</label>
		<CopyPasswordField
			name="postgresqlUser"
			id="postgresqlUser"
			value={service.hasura.postgresqlUser}
			readonly
			disabled
		/>
	</div>
	<div class="grid grid-cols-2 items-center lg:px-10 px-2">
		<label for="postgresqlPassword">{$t('forms.password')}</label>
		<CopyPasswordField
			id="postgresqlPassword"
			isPasswordField
			readonly
			disabled
			name="postgresqlPassword"
			value={service.hasura.postgresqlPassword}
		/>
	</div>
	<div class="grid grid-cols-2 items-center lg:px-10 px-2">
		<label for="postgresqlDatabase">{$t('index.database')}</label>
		<CopyPasswordField
			name="postgresqlDatabase"
			id="postgresqlDatabase"
			value={service.hasura.postgresqlDatabase}
			readonly
			disabled
		/>
	</div>
</div>
