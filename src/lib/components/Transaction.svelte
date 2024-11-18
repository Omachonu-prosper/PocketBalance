<script>
    import Icon from '@iconify/svelte';

    let { title, date, badgeColour, amount, currency = '₦' } = $props()
</script>

<div class="flex items-center mb-5">
    <Icon icon="grommet-icons:transaction" class="{badgeColour} rounded-full size-10 p-2 text-white"/>
    
    <div class="flex-auto mx-2">
        <div class="text-sm">{title}</div>
        <div class="text-xs">{date}</div>
    </div>
    
    <div class="text-sm">
        {currency}{amount}
    </div>
</div>