<script>
    import Icon from '@iconify/svelte';
    import AssetCard from '$lib/components/AssetCard.svelte';
    import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>Dashboard | PocketBalance</title>
</svelte:head>

<section class="max-w-md container mx-auto p-3 pt-1">
    <header class="flex pt-1 items-center">
        <h2 class="text-xl flex-auto">Hello User</h2>

        <Icon icon="solar:moon-stars-bold" class="text-3xl" />
    </header>

    <main class="mt-5">
        <AssetCard type='Funds' amount="30,000" button1="Add funds" button2="Reduce funds" 
            cardColour='bg-blue-700', buttonColour='bg-blue-900' />

        <AssetCard type='Debts' amount="30,000" button1="Increase debt" button2="Reduce debt"
            cardColour='bg-red-500' buttonColour='bg-red-700' />

        <AssetCard type='Savings' amount="30,000" button1="Save" button2="Withdraw"
            cardColour='bg-neutral-700' buttonColour='bg-neutral-900' currency='$' />
    </main>
</section>

<Footer active='home' />