<template>
  <div :data-theme="colorMode.value">
    <div class="flex justify-between items-center p-4">
      <h1 class="text-2xl font-bold">My Nuxt App</h1>
      <button @click="toggleDarkMode" class="btn btn-ghost">
        {{ colorMode.value === 'dark' ? '🌙' : '☀️' }}
      </button>
    </div>
    <div class="card card-compact bg-base-100 w-96 shadow-xl mx-auto">
      <figure>
        <img src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp" alt="Shoes" />
      </figure>
      <div class="card-body">
        <h2 class="card-title">Shoes!</h2>
        <p>If a dog chews shoes whose shoes does he choose?</p>
        <div class="card-actions justify-end">
          <button class="btn btn-primary">
            <span class="loading loading-spinner"></span>
            Buy Now
          </button>
        </div>
      </div>
    </div>
  </div>
  <div class="carousel carousel-center bg-whites rounded-boxs max-w-mds space-x-6 px-20">
    <div class="carousel-item" v-for="m in 10" :key="m">
      <img src="https://img.daisyui.com/images/stock/photo-1559703248-dcaaec9fab78.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1565098772267-60af42b81ef2.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1572635148818-ef6fd45eb394.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1494253109108-2e30c049369b.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1550258987-190a2d41a8ba.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1559181567-c3190ca9959b.webp" class="rounded-box" />
    </div>
    <div class="carousel-item">
      <img src="https://img.daisyui.com/images/stock/photo-1601004890684-d8cbf643f5f2.webp" class="rounded-box" />
    </div>
  </div>
</template>

<script setup>
const colorMode = useColorMode()

// Initialize with system preference, fallback to light
colorMode.value = colorMode.value || 'light'

const toggleDarkMode = () => {
  colorMode.value = colorMode.value === 'light' ? 'dark' : 'light'
}
</script>
