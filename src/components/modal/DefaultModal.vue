<script>
	export default {
		name: 'DefaultModal',
		props: {
			visible: Boolean,
			variant: String,
		},
		data(){
			return{
				ModalState: this.visible
			}
		},
		methods:{
			ToogleModal(){
				this.ModalState = false;
			},
		},
		watch: { 
			visible: function(newVal, oldVal) {
				this.ModalState = newVal;
				console.log('new' + newVal + '==' + oldVal)
			}
		}
	}
</script>

<template>
	<div>
		<!-- Modal -->
		"Modal State = " {{ this.ModalState }}
		<div v-if="ModalState" class="modal fade show d-block" 
		 tabindex="-1" aria-labelledby="modalLabel" aria-modal="true" role="dialog">
		  <div class="modal-dialog modal-dialog-centered ml-0">
		    <div class="modal-content rounded-0">
		      <div class="modal-header border-bottom-0 p-custom">
		        
		        <button type="button" @click="ToogleModal()" class="btn-close" ></button>
		      </div>
		      <div class="modal-body text-dark p-custom">
		       <slot></slot>
		      </div>
		      <div class="modal-footer border-top-0 d-flex justify-content-start p-custom">
		        <button type="button" class="btn btn-custom" >READ MORE</button>
		      </div>
		    </div>
		  </div>
		</div>
	</div>
</template>

<style scoped>
	.p-custom {

	}

	.btn-custom{
		color: #fff;
		background: rgb(97,24,24);
		background: linear-gradient(90deg, rgba(97,24,24,1) 0%, rgba(162,102,83,1) 100%);
		border-color: #918f8f;
		font-size: 18px;
		font-weight: normal;
		letter-spacing: 0.05em;
		border-radius: 0;
		padding: 10px 50px;
  		transition: all 0.5s;
	}

	.btn-custom:hover,
	.btn-custom:active,
	.btn-custom:focus,
	.btn-custom.active {
		background: rgb(97,24,24);
		background: linear-gradient(90deg, rgba(97,24,24,1) 0%, rgba(162,102,83,1) 100%);
		color: #ffffff;
		border-color: #003D4F;
	}
</style>