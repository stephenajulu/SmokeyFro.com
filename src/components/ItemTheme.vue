<template>
	<article class="item" :class="post.group">
		<g-link :to="`${post.path}`" class="block overflow-hidden transition-all duration-100 ease-out border-2 border-white rounded-md shadow-md hover:shadow-xl image">
			<div class="relative flex items-center justify-center w-full h-64 card-image" v-if="post.thumb">
				<g-image :src="post.thumb" class="absolute top-0 bottom-0 left-0 right-0 block object-cover w-full h-64" />
				<h2 class="relative z-20 px-3 py-1 m-0 mt-5 text-2xl rounded-md shadow-md bg-accent">{{ post.title }}</h2>
			</div>
		</g-link>
	</article>
</template>

<script>
import Browser from "@/components/Browser";
export default {
	components: {
		Browser
	},
	props: {
		post: {
			type: Object,
			required: true
		}
	}
}
</script>