<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";

  let y;
  let innerHeight = 0;
  let innerWidth = 0;

  function goTop() {
    document.body.scrollIntoView({ behavior: "smooth" });
  }
</script>

<div
  class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm
sm:text-base"
>
  <div
    class={`fixed bottom-8 right-8 z-50 duration-200 ${
      y <= 0
        ? "opacity-0 pointer-events-none"
        : "opacity-full pointer-events-auto"
    }`}
  >
    <button
      on:click={goTop}
      class="ml-auto rounded-full aspect-square bg-blue-900
    text-green-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer"
    >
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square" />
    </button>
  </div>
  <Header {y} />
  <slot />
  <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
