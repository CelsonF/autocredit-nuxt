<script  lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
	props: {
		content: Object,
	},
})

</script>

<template>
	<div class="modal fade" id="modalService" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1"
		aria-labelledby="modalServiceLabel" aria-hidden="true">
		<div class="modal-dialog modal-dialog-centered">
			<div class="modal-content">
				<div class="modal-header">
					<h1 class="modal-title fs-5" id="modalServiceLabel">{{ content?.title }}</h1>
					<button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
				</div>
				<div class="modal-body">
					{{ content?.content }}
				</div>
			</div>
		</div>
	</div>
</template>
