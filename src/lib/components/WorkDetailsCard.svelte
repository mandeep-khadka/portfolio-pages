<script>
	import Card, { Content } from '@smui/card';
	import List, { Item, Text, PrimaryText, SecondaryText } from '@smui/list';

    import jobs from "$lib/data/job_experience";
</script>

<div>
	<Card variant="outlined" padded>
		<Content>
			<Card padded style="color:red; font-size:25px; font-weight:bold;">Work Experience</Card>
			<div>
				<List threeLine nonInteractive>
					{#each jobs as job}
						<Item>
							<Text>
								<PrimaryText>{job.title}</PrimaryText>
								<SecondaryText>{job.start_year} - {job.end_year}</SecondaryText>
								<SecondaryText>
									{job.company}, {job.location}
								</SecondaryText>
							</Text>
						</Item>
					{/each}
				</List>
			</div>
		</Content>
	</Card>
</div>
