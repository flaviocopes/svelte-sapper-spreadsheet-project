<script context="module">
	export async function preload({ params }) {
		const { id } = params
		return { id }
	}
</script>

<script>
export let id
import Table from '../../components/Table.svelte';
</script>

<Table tableIdentifier={id} />
