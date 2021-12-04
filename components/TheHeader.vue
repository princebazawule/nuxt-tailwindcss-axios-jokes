<template>
    <header class="text-gray-600 body-font lg:w-full">
        <div class="min-w-full flex flex-wrap p-5 flex-col md:flex-row items-center">
            <NuxtLink to="/">
                <h1 class="flex title-font font-bold text-2xl items-center text-gray-900 mb-4 md:mb-0">
                    Nuxt Jokes
                </h1>
            </NuxtLink>

            <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
                <NuxtLink to="/">
                    <a class="transition duration-300 mr-5 py-1 px-2 rounded font-semibold text-black cursor-pointer hover:bg-gray-100 hover:text-indigo-600">
                        Home
                    </a>
                </NuxtLink>

                <NuxtLink to="/jokes">
                    <a class="transition duration-300 mr-5 py-1 px-2 rounded font-semibold text-black cursor-pointer hover:bg-gray-100 hover:text-indigo-600">
                        Jokes
                    </a>
                </NuxtLink>

                <NuxtLink to="/about">
                    <a class="transition duration-300 mr-5 py-1 px-2 rounded font-semibold text-black cursor-pointer hover:bg-gray-100 hover:text-indigo-600">
                        About
                    </a>
                </NuxtLink>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: "TheHeader",
};
</script>
