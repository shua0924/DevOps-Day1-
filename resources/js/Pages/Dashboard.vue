<script setup lang="ts">

const users = [
    { id: 1, name: "John Doe", email: "john@example.com", created_at: "2025-01-01" },
    { id: 2, name: "Jane Smith", email: "jane@example.com", created_at: "2025-01-05" },
    { id: 3, name: "Carlos Reyes", email: "carlos@example.com", created_at: "2025-01-08" },
];
</script>

<template>
    <div class="p-4">
        <div class="overflow-x-auto rounded-lg border border-gray-300 dark:border-gray-700">
            <table class="min-w-full divide-y divide-gray-300 dark:divide-gray-700">
                <thead class="bg-gray-100 dark:bg-gray-800">
                    <tr>
                        <th class="px-4 py-2 text-left text-sm font-semibold">ID</th>
                        <th class="px-4 py-2 text-left text-sm font-semibold">Name</th>
                        <th class="px-4 py-2 text-left text-sm font-semibold">Email</th>
                        <th class="px-4 py-2 text-left text-sm font-semibold">Created At</th>
                    </tr>
                </thead>

                <tbody class="divide-y divide-gray-200 dark:divide-gray-700">
                    <tr v-for="user in users" :key="user.id">
                        <td class="px-4 py-2 text-sm">{{ user.id }}</td>
                        <td class="px-4 py-2 text-sm">{{ user.name }}</td>
                        <td class="px-4 py-2 text-sm">{{ user.email }}</td>
                        <td class="px-4 py-2 text-sm">{{ user.created_at }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>
