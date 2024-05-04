<template>
    <div class="table-wrapper">
        <table class="user-table">
            <tr>
                <th v-for="(header, i) in headers" :key="`${header}${i}`" class="header-item">
                    {{ header }}
                </th>
            </tr>
            <tr v-for="entity in data" :key="`entity-${entity.firstName}`" class="table-rows">
                <td v-for="(header, i) in headers" :key="`${header}-${i}`">
                    <slot :name="`column${i}`" :entity="entity"></slot>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
    name: 'Table',
    props: {
        headers: {
            type: Array,
            required: true,
        },
        data: {
            type: Array,
            required: true,
        },
    },
})
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    // text-align: center;
    // background-color: #2c3e50;
    //   background-color: "#ffffff";
}

body {
    margin: 0; // background-color: #2c3e50;
}

table {
    border-collapse: separate;
    border-spacing: 0;
}

.user-table {
    border: solid 3px #7BC4E0;
    border-collapse: separate;
    width: 100%;
    border-radius: 20px;
}

th {
    background-color: #7BC4E0;
    border-top: none;
    color: white;
    font-size: 18px;
    height: 40px;
    padding-left: 16px;
    text-align: left;
}

th:first-child {
    border-left: none;
    border-top-left-radius: 16px;
}

th:last-child {
    border-top-right-radius: 16px;
}

tr:last-child {
    border-bottom-left-radius: 16px;
}

td {
    background-color: white;
    border-bottom: solid 1px grey;
    height: 40px;
    padding-left: 16px;
}

// tr:first-child td:first-child {
//     border-top-left-radius: 20px;
// }

// tr:first-child td:last-child {
//     border-top-right-radius: 20px;
// }

tr:last-child td:first-child {
    border-bottom-left-radius: 20px;
}

tr:last-child td:last-child {
    border-bottom-right-radius: 20px;
    border: none;
}

.table-wrapper {
    display: flex;
    width: 70%;
    border: none;
}
</style>