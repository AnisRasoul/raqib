<template>
    <div class="flex flex-col md:flex-row items-center p-6 bg-white shadow-lg rounded-lg">
        <div class="md:w-1/2 p-4">
            <h2 class="text-2xl font-bold mb-4">Product Title</h2>
            <p class="text-gray-700 mb-4">
                This is a brief description of the product. Highlight its features and benefits to attract potential customers.
            </p>
            <button class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
                Learn More
            </button>
        </div>
        <div class="md:w-1/2 p-4">
            <img src="https://placehold.co/600x400" alt="Product Image" class="w-full h-auto rounded-lg shadow-md">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Showcase'
}
</script>
