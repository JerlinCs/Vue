<template>
    <div>
        <v-data-table class="custom-table" theme="dark">
            <thead class="head">
                <tr>
                    <th>Roll Number</th>
                    <th>Name</th>
                    <th>Address</th>
                    <th>Phone Number</th>
                </tr>
            </thead>
            <tbody class="body">
                <tr>
                    <td>111803</td>
                    <td>Jerlin Cs</td>
                    <td>Kanyakumari</td>
                    <td>9858748908</td>
                </tr>
                <tr>
                    <td>231803</td>
                    <td>Jeffrin JP</td>
                    <td>Kanyakumari</td>
                    <td>8577938843</td>
                </tr>
                <tr>
                    <td>111850</td>
                    <td>Manoj Kumar</td>
                    <td>Madurai</td>
                    <td>8577938380</td>
                </tr>
            </tbody>
        </v-data-table>
    </div>
</template>

<script>

export default {
    name: 'MyTable',
}

</script>

<style scoped>
.body {
    color: brown;
}
.head {
    color: black;
}
.custom-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

.custom-table th, .custom-table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

.custom-table th {
  background-color: #f2f2f2;
}

.custom-table tbody tr:hover {
  background-color: #f5f5f5;
}

</style>