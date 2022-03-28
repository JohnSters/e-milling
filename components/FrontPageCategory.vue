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
            flat
					>
						<v-img
							src="/products/image1.jpg"
							:aspect-ratio="16/9"
              max-height="400"
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
            flat
					>
						<v-img
							src="/products/image2.jpg"
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
            flat
					>
						<v-img
							src="/products/image3.jpg"
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
