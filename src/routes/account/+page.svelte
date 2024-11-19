<script>
    import Icon from '@iconify/svelte';
    import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>My account | PocketBalance</title>
</svelte:head>

<section class="max-w-md container mx-auto p-3 pt-1">
    <header class="pt-1">
        <h2 class="text-md text-center">My account</h2>
    </header>

    <main class="mt-5">
        <div class="flex justify-center">
            <Icon icon="ic:round-account-circle" class="size-32 text-neutral-400 mb-5" />
        </div>

        <div class="h-80 rounded-xl bg-neutral-200">

        </div>

        <a href="/login" class="border border-red-400 w-full inline-block py-3 text-center mt-5 rounded-xl text-red-600 hover:text-white hover:bg-red-600 focus:text-white focus:bg-red-600 focus:outline-none transition-all">
            Logout
        </a>        
    </main>
</section>

<Footer active='account' />