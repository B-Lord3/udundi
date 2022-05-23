<script>
	import DefaultModal  from './DefaultModal.vue'

	export default {
		name: 'ModalAlert',
		components: {
			DefaultModal
		},
		props: {
			msg: String,
			visible: Boolean,
		},
		created() {
			console.log(this.visible);
		},
		computed: {

		},
	}
</script>

<template>
	<DefaultModal :msg="msg" :visible="visible">
		<p class="text-left">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? </p>
	</DefaultModal>
</template>

<style scoped>
	p {
	    font-size: 14px;
	    letter-spacing: 1px;
	    word-spacing: 3px;
	    line-height: 2em;
	}
</style>