<script lang="ts">
	//@ts-nocheck
	import FilterBtn from "$lib/FilterBtn.svelte";
</script>

<section class="pl-10">
	<div class="app-actions-line">
		<div class="w-5/6 lg:w-1/2 flex gap-0 rounded glass mx-auto">
			<input
				type="text"
				class="flex-grow !bg-transparent pl-2 text-white focus:outline-none overflow-hidden"
				placeholder="Search..."
			/>
			<button class="loaction-btn glass">
				<svg
					class="btn-icon"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					id=" feather-map-pin"
					viewBox="0 0 24 24"
				>
					<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z" />
					<circle cx="12" cy="10" r="3" />
				</svg>
			</button>
		</div>
		<div class="contact-actions-wrapper !hidden">
			<div class="contact-actions">
				<span>Contact us: </span>
				<a href="#" class="contact-link">
					<svg
						class="btn-icon"
						xmlns="http://www.w3.org/2000/svg"
						width="24"
						height="24"
						viewBox="0 0 24 24"
						fill="currentColor"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						id=" feather-phone"
						><path
							d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
						/></svg
					>
				</a>
				<a href="#" class="contact-link">
					<svg
						class="btn-icon"
						xmlns="http://www.w3.org/2000/svg"
						fill="currentColor"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						id=" feather-message-circle"
						viewBox="0 0 24 24"
					>
						<path
							d="M21 11.5a8.38 8.38 0 01-.9 3.8 8.5 8.5 0 01-7.6 4.7 8.38 8.38 0 01-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 01-.9-3.8 8.5 8.5 0 014.7-7.6 8.38 8.38 0 013.8-.9h.5a8.48 8.48 0 018 8v.5z"
						/>
					</svg>
				</a>
			</div>
			<div class="contact-actions socials">
				<span>Follow us: </span>
				<a href="#" class="contact-link facebook">
					<svg
						class="btn-icon"
						xmlns="http://www.w3.org/2000/svg"
						width="24"
						height="24"
						viewBox="0 0 24 24"
						fill="currentColor"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						id=" feather-facebook"
						><path
							d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"
						/></svg
					>
				</a>
				<a href="#" class="contact-link">
					<svg
						class="btn-icon"
						xmlns="http://www.w3.org/2000/svg"
						fill="currentColor"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						id=" feather-twitter"
						viewBox="0 0 24 24"
					>
						<path
							d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"
						/>
					</svg>
				</a>
			</div>
		</div>
	</div>
	<div class="app-actions-line filter-line">
		<div
			class="filter-action-buttons overflow-y-auto flex gap-2 w-fit mx-auto"
		>
			<FilterBtn />
			<FilterBtn />
			<button class="filter-btn more !hidden">
				<div class="filter-icon">
					<svg
						class="btn-icon"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						id=" feather-sliders"
						viewBox="0 0 24 24"
					>
						<path
							d="M4 21v-7M4 10V3M12 21v-9M12 8V3M20 21v-5M20 12V3M1 14h6M9 8h6M17 16h6"
						/>
					</svg>
				</div>
				<span class="filter-text">More</span>
			</button>
		</div>
	</div>
</section>
