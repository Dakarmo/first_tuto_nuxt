<template>
    
 <div>
        <nav class=" flex justify-between mb-4 items-center">
            <h2 class="mb-0">Mes Liens</h2>
            <!-- <SearchInput :modelValue="search" @update:modelValue="$event => search"/> -->
            <div class="flex items-center gap-3 justify-end">
                <SearchInput :modelValue="search"  />
                <NuxtLink to="/links/create" class="no-underline px-4 py-2 text-white bg-gray-500 hover:bg-gray-800 rounded-md transition duration-300">Créer un lien</NuxtLink>
            </div>
        </nav>
        <div v-if="true">
            <table class="w-full boder text-sm text-sm text-left text-gray-500">
                <thead class="text-xs text-gay-700 uppercase bg-gray-50">
                    <tr>
                        <th >Lien complet</th>
                        <th >Lien Court</th>
                        <th >Nbr. Vues</th>
                        <th >Supprimer</th>
                        <th >Editer</th>
                        <th  aria-label="Rafraichir">
                            <Icon name="mdi:refresh" class="w-6 h-6"/>
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="link in links" :key="link.id" class="bg-white border-b">
                        <td>
                            <a :href="link.full_links" target="_blank">
                                {{ link.full_links }}
                            </a>
                        </td>
                        <td>
                            <a :href="`${useRuntimeConfig().public.appUrl}/${link.short_links}`" target="_blank">
                                {{ `${useRuntimeConfig().public.appUrl.replace(/^http(s?):\/\//, "")}/${link.short_links}` }}
                            </a>
                        </td>
                        <td>
                            {{ link.views }}
                        </td>
                        <td>
                            <Icon name="mdi:trash" class="w-6 h-6 text-red-500"/>
                        </td>
                        <td>
                            <NuxtLink :to="`/links/${link.id}`">
                                <Icon class="w-6 h-6 text-green-500" name="material-symbols:edit-square-outline" />
                            </NuxtLink>
                        </td>
                        <td> </td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div v-else>
            <Icon name="" />
            <p>
                <!-- Afficher si on entre un term de recherche et qu'on ne trouve rien -->
                <span v-if="true">Aucun lien ne correspond à votre recherche.</span> 

                <!-- Afficher si au chargement de la page aucun lien n'est tretourné de la BDD -->
                <span v-else>Aucun créé pour le moment.
                    <NuxtLink to="#" class="text-blue-600 underline"> Créer votre lien</NuxtLink>
                </span> 
            </p>
        </div>
    </div>
</template>
<script lang="ts" setup>


    const links = [
        {
            short_links: "lk34oigfd",
            full_links: "https://youtube.com",
            views: 3,
            id: 1,

        },
        {
            short_links: "rtg244fgh",
            full_links: "https://w3school.com",
            views: 1,
            id: 2,
        },
        {
            short_links: "5d4fghhder",
            full_links: "https://devdocs.io",
            views: 0,
            id: 3,
        }
    ];

    const search = ref("");
</script>

<style scoped>
th {
    @apply px-6 py-3
}
td {
    @apply px-6 py-4
}
    
</style>