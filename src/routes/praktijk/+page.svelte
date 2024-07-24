<script lang="ts">

    import Leaflet from '$lib/components/Leaflet.svelte';

    import praktijk1 from "$lib/images/praktijk_1.jpeg";
    import praktijk2 from "$lib/images/praktijk_2.jpeg";
    import praktijk3 from "$lib/images/praktijk_3.jpeg";

</script>

<svelte:head>
    <title>Praktijk | Dr. Lebbe</title>

    <meta property="og:url" content="https://dr-lebbe.be/praktijk">
    <meta property="og:title" content="Dr. Lebbe - Praktijk">
    <meta property="og:description" content="Locatie, parking & betalen bij Dr. Lebbe">
</svelte:head>

<div class="bg-white">
    <div class="max-w-screen-lg mx-auto flex">

        <div class="flex flex-col px-8 mb-10 w-full text-leb-grey-950 font-jost text-lg">

            <h2 class="text-xl font-medium text-center mt-6 mb-6 md:text-start">Locatie</h2>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

                <div class="flex flex-col">
                    <p>De praktijk van Dr Lebbe vindt u op het adres: <br/><span class="font-medium">Potterierei 60, centrum Brugge</span>.</p>

                    <div class="my-6">
                    <a target="_blank" href="https://www.google.com/maps/place/Dr.+Barbara+Lebbe/@51.2173036,3.228994,17z/data=!3m1!4b1!4m6!3m5!1s0x47c3513937fb1e1d:0xd358d22dafffbb93!8m2!3d51.2173036!4d3.228994!16s%2Fg%2F11l2p2hqzx?entry=ttu"
                       class="inline-block bg-leb-blue-100 hover:bg-leb-blue-50 active:bg-leb-blue-200 transition duration-100 text-leb-blue-500 text-lg pl-8 pr-6 py-3 rounded-md">
                        Google maps <i class="material-symbols-rounded align-text-bottom ml-1">open_in_new</i>
                    </a>
                    </div>


                    <div class="w-full h-64 md:h-full md:grow">
                        <Leaflet />
                    </div>

                </div>

                <div class="grid grid-cols-2 gap-6 md:gap-4">

                    <img class="rounded-md col-span-2 object-cover h-60 w-full" src={praktijk1} alt="Praktijk 1">

                    <img class="rounded-md object-cover h-60 w-full" src={praktijk2} alt="Praktijk 2">
                    <img class="rounded-md object-cover h-60 w-full" src={praktijk3} alt="Praktijk 3">

                </div>

            </div>

            <div class="mt-16 space-y-6">
                <h2 class="text-xl font-medium text-center mb-4 md:mb-2 md:text-start">Parkeren</h2>

                <p>Er is steeds voldoende parkeergelegenheid ter hoogte van het Grootseminarie, of aan de overzijde van het water langs de Langerei.</p>

                <p>Opgepast: in de binnenstad geldt elke dag betalend parkeren van 9u tot 20u. U kunt betalen aan een automaat, via SMS of <a class="underline" href="https://4411.be/nl-be/download-app" target="_blank">de 4411 app</a>. Meer informatie kunt u vinden op <a class="underline" href="https://www.brugge.be/mobiliteit/parkeren/vind-een-parking/parkeerautomaten" target="_blank">de website van stad Brugge</a>.</p>
            </div>

            <div class="mt-16 space-y-6">
                <h2 class="text-xl font-medium text-center mb-4 md:mb-2 md:text-start">Betalen</h2>

                <p>Gelieve steeds elektronisch te betalen. Dit is veiliger. U kunt vlot betalen met <a class="underline" href="https://www.payconiq.be/nl/particulier/mobiel-betalen" target="_blank">Payconic</a> of bankkaart.</p>
            </div>

        </div>

    </div>
</div>
