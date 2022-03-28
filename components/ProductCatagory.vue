<template>
	<div>
		<v-container>
			<h1 class="grey--text text--darken-2">Product Range</h1>
			<v-row>
				<v-col
					cols="12"
					sm="4"
				>
					<v-card
						class="mx-auto pa-2"
						max-width="450"
            flat
					>
						<v-img
							src="/products/lucky.jpg"
							:aspect-ratio="16/9"
						>
						</v-img>
						<v-card-title>
							<div class="text-h5 font-weight-regular grey--text">
								Lucky
							</div>
						</v-card-title>
					</v-card>
				</v-col>
				<v-col
						cols="12"
						sm="4"
				>
					<v-card
						class="mx-auto pa-2"
						max-width="450"
            flat
					>
						<v-img
							src="/products/super.jpg"
							:aspect-ratio="16/9"
						>
						</v-img>
						<v-card-title>
							<div class="text-h5 font-weight-regular grey--text">
								Super Life
							</div>
						</v-card-title>
					</v-card>
				</v-col>
				<v-col
					cols="12"
					sm="4"
				>
					<v-card
						class="mx-auto pa-2"
						max-width="450"
            flat
					>
						<v-img
							src="/products/Hippo.jpg"
							:aspect-ratio="16/9"
						>
						</v-img>
						<v-card-title>
							<div class="text-h5 font-weight-regular grey--text">
								Hippo Samp
							</div>
						</v-card-title>
					</v-card>
				</v-col>
					<v-col class="flaot-right green--text mt-5 text-h6">View more ></v-col>
			</v-row>
		</v-container>
	</div>
</template>
