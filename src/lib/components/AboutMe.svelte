<script lang="ts">
	import { Button, Experience, SectionHeader } from '$components';
	import image from '$assets/me.jpg';
	import { goto } from '$app/navigation';

	type AboutMeProps = {
		workExperience: DevExperience[];
	};

	let { workExperience }: AboutMeProps = $props();

	function onclick() {
		goto('/#my-projects');
	}
</script>

<section class="mt-16">
	<SectionHeader sectionName="about-me">About Me</SectionHeader>
	<div class="mt-6 flex flex-col md:flex-row md:space-x-16">
		<img class="object-cover shadow-md md:w-1/3" src={image} alt="author" />
		<div class="text-left">
			<p>
				Tech and Travel have always been my two main passions in life since I was in high school.
				Luckily as a Software Engineer, combining them has been relatively easy.
			</p>
			<p>
				With over 12 years of relevant professional software experience working at both startups and
				large corporations, I have amassed a relatively large tool set to solve various problems
				that could arise in the world of software devleopment. Ever since I got my first Android
				smartphone, I was drawn to the world of mobile software development. It took a lot of
				nudging for me to do dive into the wild wild world of web development, but I don't regret
				taking the plunge.
			</p>
			<Button {onclick} className="mt-8">View Projects</Button>
		</div>
	</div>
	<Experience {workExperience} />
</section>
