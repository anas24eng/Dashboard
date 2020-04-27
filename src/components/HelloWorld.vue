<template>
	<v-container>
		<v-layout text-center wrap>
			<v-flex xs12>
				<v-img
					:src="require('../assets/logo.svg')"
					class="my-3"
					contain
					height="200"
				></v-img>
			</v-flex>

			<v-flex mb-4>
				<h1 class="display-2 font-weight-bold mb-3">
					Welcome to Cars's App
				</h1>
				<p class="subheading font-weight-regular">
					For	More Information Vist our page on Facebook in link below ,
					<br />please join our online
					<a href="https://community.facebook.com" target="_blank"
						>facebook Community</a
					>
				</p>
			</v-flex>

			<v-flex mb-5 xs12>
				<h2 class="headline font-weight-bold mb-3">What's next?</h2>

				<v-layout justify-center>
					<a
						v-for="(next, i) in whatsNext"
						:key="i"
						:href="next.href"
						class="subheading mx-3"
						target="_blank"
					>
						{{ next.text }}
					</a>
				</v-layout>
			</v-flex>

			<v-flex xs12 mb-5>
				<h2 class="headline font-weight-bold mb-3">Important Links</h2>

				<v-layout justify-center>
					<a
						v-for="(link, i) in importantLinks"
						:key="i"
						:href="link.href"
						class="subheading mx-3"
						target="_blank"
					>
						{{ link.text }}
					</a>
				</v-layout>
			</v-flex>

			<v-flex xs12 mb-5>
				<h2 class="headline font-weight-bold mb-3">Socail Media</h2>

				<v-layout justify-center>
					<a
						v-for="(eco, i) in ecosystem"
						:key="i"
						:href="eco.href"
						class="subheading mx-3"
						target="_blank"
					>
						{{ eco.text }}
					</a>
				</v-layout>
			</v-flex>
		</v-layout>
	</v-container>
</template>

<script>
export default {
	data: () => ({
		ecosystem: [
			{
				text: 'SnapChat',
				href: 'https://SnapChat.com'
			},
			{
				text: 'instagram',
				href: 'https://instagram.com'
			},
			{
				text: 'LinkedIn',
				href: 'https://LinkedIn.com'
			}
		],
		importantLinks: [
			{
				text: 'Documentation',
				href: 'https://Cars.com'
			},
			{
				text: 'Chat',
				href: 'https://community.com'
			},
			{
				text: 'eBay',
				href: 'https://eBay.com'
			},
			{
				text: 'Twitter',
				href: 'https://twitter.com'
			},
			{
				text: 'Articles',
				href: 'https://medium.com'
			}
		],
		whatsNext: [
			{
				text: 'Explore items',
				href: 'https://cars.com'
			},
			{
				text: 'Select a Item',
				href: 'https://Item.com/layout'
			},
			{
				text: 'Frequently Asked Questions',
				href: 'https://cars.com/getting-started/frequently-asked-questions'
			}
		]
	})
}
</script>