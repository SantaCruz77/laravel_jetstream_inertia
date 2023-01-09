<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
defineProps({
    blogs: Array,
});
</script>

<template>
    <AppLayout title="Blog">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Blog
            </h2>
        </template>
        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <table>
                    <thead>
                        <tr>
                            <th>タイトル</th>
                            <th>コンテンツ</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="blog in blogs" :key="blog.id">
                            <td class="border px-4 py-2">{{ blog.title }}</td>
                            <td class="border px-4 py-2">{{ blog.content }}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </AppLayout>
</template>
