<script lang="ts">

    import {Hamburger} from 'svelte-hamburgers';
    import {page as currentPage} from '$app/stores';
    import logo from "$lib/images/logo.svg";
    import Menu from "$lib/components/Menu.svelte";
    import { navigating } from '$app/stores';

    $: if($navigating) closeMenu();

    let y: number;
    let open: boolean;

    function closeMenu() {
        open = false;
    }

</script>

<svelte:window bind:scrollY={y}/>

<header class="{y > 50 ? 'bg-white/80 backdrop-blur drop-shadow-md' : 'bg-white'} sticky top-0 z-[2000] transition duration-500">

    <div class="max-w-screen-lg mx-auto flex items-center px-8 pt-10 pb-10">

        <a href="/">
            <img class="max-h-14" src={logo} alt="Logo Dr. Lebbe">
        </a>

        <div class="flex-grow"></div>

        <div class="hidden md:flex flex-row justify-center space-x-8">

            <!-- Over -->
            {#if $currentPage.url.pathname === '/'}
                <a class="font-albert text-lg uppercase text-leb-blue-400" href="/">
                    Over
                    <span class="block max-w-full h-0.5 bg-leb-blue-400"></span>
                </a>
            {:else}
                <a class="font-albert text-lg uppercase text-leb-grey-950 group transition duration-100 hover:text-leb-blue-400"
                   href="/">
                    Over
                    <span class="block max-w-0 group-hover:max-w-full transition-all duration-150 h-0.5 bg-leb-blue-400"></span>
                </a>
            {/if}

            <!-- Praktijk -->
            {#if $currentPage.url.pathname === '/praktijk'}
                <a class="font-albert text-lg uppercase text-leb-blue-400" href="/praktijk">
                    Praktijk
                    <span class="block max-w-full h-0.5 bg-leb-blue-400"></span>
                </a>
            {:else}
                <a class="font-albert text-lg uppercase text-leb-grey-950 group transition duration-100 hover:text-leb-blue-400"
                   href="/praktijk">
                    Praktijk
                    <span class="block max-w-0 group-hover:max-w-full transition-all duration-150 h-0.5 bg-leb-blue-400"></span>
                </a>
            {/if}

        </div>

        <div class="-mr-2 md:hidden">
            <Hamburger bind:open --border-radius="0px" --color="#353B40" --layer-height="2px"/>
            <Menu bind:open />
        </div>

    </div>

</header>
