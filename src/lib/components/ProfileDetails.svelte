<script>
	import LayoutGrid, { Cell } from '@smui/layout-grid';
	import WorkDetailsCard from './WorkDetailsCard.svelte';
    import EducationDetailsCard from './EducationDetailsCard.svelte';
</script>

<LayoutGrid>
	<Cell span={9}>
		<WorkDetailsCard/>
	</Cell>
</LayoutGrid>
<LayoutGrid>
	<Cell span={9}>
		<EducationDetailsCard/>
	</Cell>
</LayoutGrid>
