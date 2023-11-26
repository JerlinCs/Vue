<template>
    <div>
        <table class="tableHead">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Address</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="employee in employees" :key="employee.id">
                    <td>{{ employee.name }}</td>
                    <td>{{ employee.address }}</td>
                    <td class="btnContainer"><button class="btnAdd">ADD</button><button class="btnDelete">DELETE</button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>

export default {
    name: 'MyComponent',
    props: {
        employees: Array
    }
}
</script>

<style scoped>
td,
th {
    border: 0.5px solid;
    width: 200px;
    background-color: wheat;
}

.btnAdd {
    color: white;
    background-color: green;
    height: 30px;
    width: 60px;
}

.btnDelete {
    color: white;
    background-color: red;
    height: 30px;
    width: 70px;
}

.btnContainer button {
    margin: 10px;
}
</style>