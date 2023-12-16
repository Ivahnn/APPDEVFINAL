<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, router } from '@inertiajs/vue3';
import { defineProps } from 'vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import TextInput from '@/Components/TextInput.vue';
import InputLabel from '@/Components/InputLabel.vue';
import { reactive } from 'vue';

const props = defineProps({
  location: Object,
});

const form = reactive({
  _method: 'put',
  location: props.location.location,
});

function validateInput() {
  // Allow only letters and spaces
  const validChars = /^[a-zA-Z\s]*$/;

  if (!validChars.test(form.location)) {
    alert("Invalid characters or numbers are not allowed.");
    return false;
  }

  return true;
}

function update() {
  if (validateInput()) {
    router.post(`/location/${props.location.id}`, {
      _method: 'put',
      location: form.location,
    });
  }
}
</script>

<template>
  <Head title="Update Location" />

  <AuthenticatedLayout>
    <div class="py-12">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <div class="overflow-hidden ma-8 w-100 bg-sky-200 rounded-lg border shadow-xs">
          <div class="overflow-x-auto mx-8">
            <form @submit.prevent="update">
              <InputLabel for="location" value="Location" />
              <TextInput
                id="code"
                type="text"
                v-model="form.location"
                required
              />
              <div class="py-3 md:w-1/3">
                <PrimaryButton>Submit</PrimaryButton>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </AuthenticatedLayout>

</template>
