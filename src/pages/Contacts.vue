<template>
  <div>
    <h1>Contacts</h1>
    <ContactListProps :contactList="contacts"/>
    <ContactDetail :contact="contact"/>
    <!-- <router-link class="btn btn-success" to="add-contact/4">Add</router-link>
    <button class="btn btn-success">Success</button> -->
  </div>
</template>

<script>
import ContactListProps from '../components/ContactListProps';
import ContactDetail from '../components/ContactDetails';

export default {
    components: {
        ContactListProps,
        ContactDetail
    },
    data() {
        return {
            contacts: [
                { id: 1, name: 'John Doe', email: 'johndoe@example.com', number: '555-12345' },
                { id: 2, name: 'Pera Peric', email: 'peraperic@example.com', number: '555-54321' },
                { id: 3, name: 'Nenad Vujicic', email: 'nenad.v@example.com', number: '555-67890' }
            ]
        };
    },

    computed: {
        contact() {
            let routeParam = this.$route.params.id;
            return this.contacts.find(contact => contact.id == routeParam);   //kraci nacin
            // let returnContact = {};
            // this.contacts.forEach(contact => {
            //     if (contact.id === routeParam) {
            //         returnContact = contact;                               //duzi nacin
            //     }
            // });
            // return returnContact;
        }
    }
}
</script>