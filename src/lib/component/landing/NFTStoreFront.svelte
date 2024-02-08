<script lang="ts">
	import Button from './components/Button.svelte';
</script>

<!-- Change the colour #f8fafc to match the previous section colour -->
<svg class="wave-top"> </svg>
<section class="container mx-auto text-center py-6 mb-12 mt-1">
  <div class="text-center mb-10">
    <div class="content justify-center items-center relative">
      <h3 class="text-1xl font-bold leading-tight text-white absolute" style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
        DragonVerse
      </h3>
      <h3 class="text-1xl font-bold leading-tight text-white absolute" style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
        DragonVerse
      </h3>
    </div>
  </div>

  <div class="relative p-2 rounded-lg shadow-md flex items-center flex-col md:flex-row">
    <img
      src="/nft-card.png"
      alt="NFT Card"
      class="mx-auto mt-4 max-w-full object-contain h-65 w-96 rounded-lg overflow-hidden border-1 shadow-glow"
    />
  </div>
  <div class="text-center mb-4 md:mb-0">
    <p class="text-white-900 mt-2">
      <span class='m-6'>
      <span class='opacity-70'>Creator:</span> 
      <span class="opacity-100 text-white">-</span>
      </span>
      <span class='m-6'>
      <span class='opacity-70'>Available:</span> 
      <span class="opacity-100 text-white">-</span>
      </span>
    </p>
  </div>
  <button class="bg-transparent mt-2 hover:bg-purple-400 text-white-700 font-semibold hover:text-white py-2 px-4 border border-white-500 hover:border-transparent rounded-full">
    MINT EGG NFT
  </button>

  <div class="w-full mb-4 mt-4">
    <p class="my-4 text-2xl text-cyan-100 leading-tight">Limited supply</p>
  </div>
</section>