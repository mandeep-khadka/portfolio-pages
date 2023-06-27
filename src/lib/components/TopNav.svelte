<script lang="ts">
    import TopAppBar, {
      Row,
      Section,
      Title
    } from '@smui/top-app-bar';
    import IconButton from '@smui/icon-button';

    import { goto } from '$app/navigation';
   
    let topAppBar: TopAppBar;
  </script>

<TopAppBar bind:this={topAppBar} variant="standard" color="secondary">
	<Row>
		<!-- <Section>
			<IconButton>
				<Icon component={Svg} viewBox="0 0 24 24">
					<path fill="currentColor" d={mdiMenu} />
				</Icon>
			</IconButton>
		</Section> -->
		<Section style="display:flex;  justify-content:space-evenly;">
				<IconButton class="material-icons" on:click={() => { goto("/") }}
					>home</IconButton
				  >
				  <IconButton class="material-icons" on:click={() => {goto("/blog")}}
					>local_library</IconButton
				  >
				  <IconButton class="material-icons" on:click={() => {goto("/projects")}}
					>rocket_launch</IconButton
				  >
				  <IconButton class="material-icons" on:click={() => {goto("/contact")}}
					>email</IconButton
				  >
		</Section>
	</Row>
</TopAppBar>

<style>
    /* Hide everything above this component. */
    :global(#smui-app),
    :global(body),
    :global(html) {
      display: block !important;
      height: auto !important;
      width: auto !important;
      position: static !important;
    }
  </style>