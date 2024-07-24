<script lang="ts">

    import {onMount, onDestroy} from 'svelte';
    import type {Map} from 'leaflet';

    import 'leaflet/dist/leaflet.css';

    let mapElement: HTMLElement;
    let map: Map;


    onMount(async () => {
        const leaflet = await import('leaflet');

        map = leaflet.map(mapElement, { attributionControl: false}).setView([51.2173036, 3.228994], 15);

        leaflet.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        }).addTo(map);

        leaflet.marker([51.2173036, 3.228994]).addTo(map);
    });


    onDestroy(async () => {
        if (map) {
            console.log('Unloading Leaflet map.');
            map.remove();
        }
    });

</script>

<div class="w-full h-full rounded-md" bind:this={mapElement}></div>



<style>

</style>



