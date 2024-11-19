<script>
    import Icon from '@iconify/svelte';

    let { 
        type, amount, button1, button2, currency = '₦',
        cardColour, buttonColour
    } = $props()
    let amountVisible = $state(false)
    let increasePopupVisible = $state(false)
    let decreasePopupVisible = $state(false)

    const toggleAmountVisible = (e) => {
        amountVisible = !amountVisible
    }

    const toggleIncreasePopup = (e) => {
        increasePopupVisible = !increasePopupVisible
    }

    const toggleDecreasePopup = (e) => {
        decreasePopupVisible = !decreasePopupVisible
    }
</script>


<div class="{cardColour} rounded-xl relative h-36 mt-8">
    <div class="px-3 pt-3">
        <p class="text-white text-xs px-1 border inline-block rounded-md">{type}</p>
        <h2 class="text-white text-2xl mt-1">
            { amountVisible ? currency + amount : '***' }
            <Icon icon={amountVisible ? 'solar:eye-bold' : 'solar:eye-closed-bold'} class="inline-block text-2xl pl-1 pb-1"
                onclick={toggleAmountVisible}/>
        </h2>
    </div>
    
    <div class="flex justify-stretch absolute bottom-2 w-full p-2">
        <button class="text-white flex-auto mx-1 p-1 rounded-xl {buttonColour}" type="button" onclick={toggleIncreasePopup}>
           {button1} <Icon icon="solar:course-up-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
        
        <button class="text-white flex-auto mx-1 p-1 rounded-xl {buttonColour}" type="button" onclick={toggleDecreasePopup}>
            {button2} <Icon icon="solar:course-down-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
    </div>
</div>

<!-- Popup that's hidden by default [Used for increasing assets] -->
<div class="h-screen fixed w-full top-0 bg-white pr-6 transition-all {increasePopupVisible ? 'block' : 'hidden'} z-10">
    <Icon icon="ic:twotone-close" class="absolute top-5 right-5 text-2xl" onclick={toggleIncreasePopup}/>
    
    <div class="{cardColour} rounded-xl mt-14 p-3">
        <input placeholder="0.00" type="number" step="0.01" min="0" inputmode="decimal"
        class="placeholder-white rounded-xl px-4 py-2 border-white border-2 bg-transparent w-full focus:border-white text-white" >
        
        <button class="text-white mx-1 p-1 px-5 mt-4 rounded-xl {buttonColour}" type="button">
            {button1} <Icon icon="solar:course-up-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
    </div>
</div>

<!-- Popup that's hidden by default [Used for reducing assets] -->
<div class="h-screen fixed w-full top-0 bg-white pr-6 transition-all {decreasePopupVisible ? 'block' : 'hidden'} z-10">
    <Icon icon="ic:twotone-close" class="absolute top-5 right-5 text-2xl" onclick={toggleDecreasePopup} />
    
    <div class="{cardColour} rounded-xl mt-14 p-3">
        <input placeholder="0.00" type="number" step="0.01" min="0" inputmode="decimal"
        class="placeholder-white rounded-xl px-4 py-2 border-white border-2 bg-transparent w-full focus:border-white text-white" >
        
        <button class="text-white mx-1 p-1 px-5 mt-4 rounded-xl {buttonColour}" type="button">
            {button2} <Icon icon="solar:course-down-broken" class="inline-block text-2xl pl-1 pb-1" />
        </button>
    </div>
</div>