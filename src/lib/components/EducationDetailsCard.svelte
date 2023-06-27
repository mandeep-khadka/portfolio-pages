<script>
	import Card, { Content } from '@smui/card';
	import List, { Item, Text, PrimaryText, SecondaryText } from '@smui/list';

	import degrees from '$lib/data/education';
</script>

<div>
	<Card variant="outlined" padded>
		<Content>
			<Card padded style="color:red; font-size:25px; font-weight:bold;">Education</Card>
			<div>
				<List threeLine nonInteractive>
					{#each degrees as degree}
						<Item>
							<Text>
								<PrimaryText>{degree.degree} {degree.title}</PrimaryText>
								<SecondaryText>{degree.start_year} - {degree.end_year}</SecondaryText>
								<SecondaryText>
									{degree.school}, {degree.location}
								</SecondaryText>
							</Text>
						</Item>
					{/each}
				</List>
			</div>
		</Content>
	</Card>
</div>
