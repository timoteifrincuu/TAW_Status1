<template>
    <div class="w-full sm:max-w-sm md:max-w-md xl:max-w-2xl p-4 bg-orange-100 rounded-lg shadow-lg mt-8">
        <h2 id="detalii-programare" class="text-2xl font-bold mb-4">Detalii programare</h2>
        <form @submit.prevent class="space-y-4">
            <div>
                <label for="appointment-date" class="block font-bold">Data</label>
                <input type="date" id="appointment-date" name="appointment-date"
                    class="w-full p-2 rounded-lg border border-orange-200">
            </div>
            <div>
                <label for="appointment-time" class="block font-bold">Ora</label>
                <input type="time" id="appointment-time" name="appointment-time"
                    class="w-full p-2 rounded-lg border border-orange-200">
            </div>

            <WatchAndComputed />

            <button type="button"
                class="w-full bg-orange-200 hover:bg-orange-100 text-orange-950 py-2 rounded-lg p-8">Anuleaza
                programare</button>
        </form>
    </div>


</template>


<script setup>
    import WatchAndComputed from './WatchAndComputed.vue'
</script>