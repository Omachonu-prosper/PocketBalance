<script>
    import Footer from '$lib/components/Footer.svelte';
    import Transaction from '$lib/components/Transaction.svelte';
</script>

<svelte:head>
  <title>Transaction history | PocketBalance</title>
</svelte:head>

<section class="max-w-md container mx-auto p-3 pt-1">
    <header class="pt-1">
        <h2 class="text-md text-center">Transaction history</h2>
    </header>

    <main class="mt-5 mb-20">
        <Transaction title="Added to funds" date="Tue Nov 19 2024 11:20:23" amount="40,000" badgeColour="bg-blue-400" />
        <Transaction title="Added to debts" date="Tue Nov 16 2024 11:20:23" amount="20,000" badgeColour="bg-red-400" />
        <Transaction title="Added to savings" date="Tue Nov 19 2024 11:20:23" amount="4,000" badgeColour="bg-neutral-400" />
        <Transaction title="Added to funds" date="Tue Nov 19 2024 11:20:23" amount="400" badgeColour="bg-blue-400" />
        <Transaction title="Added to debts" date="Tue Nov 19 2024 11:20:23" amount="230,000" badgeColour="bg-red-400" />
        <Transaction title="Removed from savings" date="Tue Nov 19 2024 11:20:23" amount="40,000" badgeColour="bg-neutral-400" currency='$'/>
    </main>
</section>

<Footer active='history' />