<script lang="ts">
    import '../app.css'
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class="w-full flex flex-col">

    <Header/>

    <slot />

    <Footer/>

</div>
