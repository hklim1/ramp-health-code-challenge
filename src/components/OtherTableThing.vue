<template>
    <table-component :headers="headers" :data="data">
        <template #column0="{ entity }">
            {{ entity.firstName }}
        </template>
        <template #column1="{ entity }">
            {{ entity.lastName }}
        </template>
        <template #column2="{ entity }">
            {{ entity.emailAddress }}
        </template>
        <template #column3="{ entity }">
            {{ entity.actions }}
        </template>
    </table-component>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TableComponent from './Table.vue'

export default defineComponent({
    components: {
        TableComponent
    },

    data: () => ({
        headers: [
            'First Name',
            'Last Name',
            'Email Address',
            'Actions'
        ],
        data: [
            {
                firstName: 'Heather',
                lastName: 'Lim',
                emailAddress: 'heather@lim.com',
                actions: '',
            },
            {
                firstName: 'Patrick',
                lastName: 'Alexander',
                emailAddress: 'patrick@alex.com',
                actions: '',
            },
            {
                firstName: 'Kwabena',
                lastName: 'Ankobiah',
                emailAddress: 'kwabena@ankobiah.com',
                actions: '',
            },
        ],
    })
})

</script>