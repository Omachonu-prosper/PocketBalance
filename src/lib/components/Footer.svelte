<script>
    import Icon from '@iconify/svelte';

    let { active } = $props()
</script>

<footer class="border border-t-gray-50 fixed bottom-0 left-0 right-0 bg-slate-50 flex justify-stretch p-3">
    <a href="#top" class="flex flex-col items-center transition flex-auto {active == 'home' ? 'text-neutral-900' : 'text-neutral-400'} hover:text-neutral-900 focus:outline-none focus:text-neutral-900">
        <Icon icon="fluent:home-20-filled" class="text-2xl" />
        <span class="text-xs">
            Home
        </span>
    </a>

    <a href="#top" class="flex flex-col items-center transition flex-auto {active == 'history' ? 'text-neutral-900' : 'text-neutral-400'} hover:text-neutral-900 focus:outline-none focus:text-neutral-900">
        <Icon icon="tabler:clock-filled" class="text-2xl" />
        <span class="text-xs">
            History
        </span>
    </a>

    <a href="#top" class="flex flex-col items-center transition flex-auto {active == 'account' ? 'text-neutral-900' : 'text-neutral-400'} hover:text-neutral-900 focus:outline-none focus:text-neutral-900">
        <Icon icon="ic:round-account-circle" class="text-2xl" />
        <span class="text-xs">
            Account
        </span>
    </a>
</footer>