<template>
    <div>
        <router-link
        class="list-group-item list-group-item-action" 
        v-for="(contact, index) in contactList" 
        :key="index" 
        :to="{name: 'contact-details', params: {id: contact.id}}"
        tag="button"
        exact-active-class="active">
            {{ contact.name }}
        </router-link>
    </div>
</template>

<script>
export default {
    props: ['contactList']
}
</script>

