<template>
    <footer class="footer text-gray-600 body-font">
        <div className="min-w-full px-5 py-8 flex items-center sm:flex-row flex-col">
            <p className="text-sm text-gray-500 sm:ml-4 sm:pl-4 sm:border-l-2 sm:border-gray-200 sm:py-2 sm:mt-0 mt-4">
                &copy; {{ new Date().getFullYear() }} — All rights reserved
            </p>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'TheFooter'
}
</script>
