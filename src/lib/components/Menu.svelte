<script lang="ts">
    import {fly} from 'svelte/transition';
    export let open: boolean;

    const links = {
        "Over": "/",
        "Praktijk": "/praktijk",
    }
</script>

{#if open}
    <div class="w-full fixed top-[136px] z-[1100] left-0 bg-leb-blue-50/80 backdrop-blur border-t-2 border-leb-blue-400">
        <div class="flex flex-col items-center space-y-8 py-8">
            {#each Object.entries(links) as [title, path], i}
                <a class="font-albert text-lg uppercase text-leb-grey-950 hover:underline" href="{path}"
                   transition:fly={{ y: -15, delay: 50 * i }}>
                    {title}
                </a>
            {/each}
        </div>
    </div>
{/if}
