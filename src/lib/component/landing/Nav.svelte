<script lang="ts">
  import { clickOutside, clickOutsideAction } from '$lib/actions/clickOutside'
  import Button from './components/Button.svelte'

  let y: number
  let navFloat = false
  $: navFloat = y > 10

  let showMenu = false
  const toggleMenu = () => (showMenu = !showMenu)
  let hambugerEl: any

  const onClickOutsideAction = ({ target }) => {
    if (!hambugerEl.contains(target)) showMenu = false
  }
  const onClickOutside = ({ detail: { event: { target } } }) => {
    if (!hambugerEl.contains(target)) showMenu = false
  }
</script>

<svelte:window bind:scrollY={y} />
<!--Nav-->
<nav
  id="header"
  class={`
  fixed w-full z-30 top-0  text-white 
  ${navFloat && 'bg-gradient-to-r from-red-950 to-black'}
  `}
>
  <div class="w-full  mx-auto mb-5 mt-4 flex flex-wrap items-center justify-between mt-0 py-2">
    <div class="pl-4 flex items-center">
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a
        class="no-underline hover:no-underline font-bold text-2xl lg:text-4xl"
        href="#"
      >
      <div class="flex items-center ml-19"> <!-- Adding ml-4 to move the entire content to the left -->
        <img
          src="/DragonVerseLogo.png"
          alt="NFT Card"
          class="max-w-full object-contain h-15 w-40 overflow-hidden border-1 shadow-glow"
        />
        <div class="ml-7 text-2xl">DEN </div> <!-- Adjusting the ml value to move the text closer to the image -->
      </div>
      
      <div class="flex justify-start">
        </div>
      </a>
    </div>
    <div bind:this={hambugerEl} class="block lg:hidden pr-4">
      <button
        on:click={toggleMenu}
        id="nav-toggle"
        class="flex items-center p-1 text-pink-800 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out"
        >
        <svg class="fill-current h-6 w-6" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
    </div>
    <!-- use:clickOutsideAction={onClickOutsideAction} -->
    <!-- use:clickOutside on:clickOutside={onClickOutside} -->
    <div
    use:clickOutside on:clickOutside={onClickOutside}
    class:hidden={!showMenu}
    class="hidden flex-grow lg:flex mr-5 lg:items-center mt-2 lg:mt-0 bg-black  lg:bg-transparent text-white lg:justify-end z-20" 
  >
  <div class="list-reset lg:flex  items-center">
    <ul> 
      <li>
        <a class="py-2 px-4  text-white font-bold hover:text-red-500 no-underline" href="/">INCUBATOR</a>
      </li>
    </ul>
    
    <button
      class="neon-button lg:mx-0" >
      Connect Wallet
    </button>
  </div>
</div>
  </div>
  <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
</nav>
