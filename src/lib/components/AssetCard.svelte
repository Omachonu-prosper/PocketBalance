<script>
    import Icon from '@iconify/svelte';

    let { 
        type, amount, button1, button2, currency = '₦',
        cardColour, buttonColour
    } = $props()
    let showing = $state(false)

    const toggleAmount = (e) => {
        showing = !showing
    }
</script>


<div class="{cardColour} rounded-xl relative h-36 mt-8">
    <div class="px-3 pt-3">
        <p class="text-white text-xs px-1 border inline-block rounded-md">{type}</p>
        <h2 class="text-white text-2xl mt-1">
            { showing ? currency + amount : '***' }
            <Icon icon={showing ? 'solar:eye-bold' : 'solar:eye-closed-bold'} class="inline-block text-2xl pl-1 pb-1"
                onclick={toggleAmount}/>
        </h2>
    </div>
    
    <div class="flex justify-stretch absolute bottom-2 w-full p-2">
        <button class="text-white flex-auto mx-1 p-1 rounded-xl {buttonColour}" type="button">
           {button1} <Icon icon="solar:course-up-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
        <button class="text-white flex-auto mx-1 p-1 rounded-xl {buttonColour}" type="button">
            {button2} <Icon icon="solar:course-down-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
    </div>
</div>