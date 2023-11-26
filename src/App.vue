<template>
  <div class="parent-container">
    <div class="small-container">
      <employee-form @add:employee="addEmployee"/>
      <MyComponent v-bind:employees="employees" />
    </div>
  </div>
</template>

<script>
import MyComponent from './components/MyComponent.vue';
import EmployeeForm from './components/EmployeeForm.vue';

export default {
  name: 'App',
  components: {
    MyComponent,
    EmployeeForm
  },

  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Jerlin',
          address: 'Kanyakumari, Nagercoil'
        },
        {
          id: 2,
          name: 'Rijil Weslin',
          address: 'Kanyakumari, Kulasegaram'
        },
        {
          id: 3,
          name: 'Manoj Kumar',
          address: 'Theni'
        },
        {
          id: 4,
          name: 'Jeffrin',
          address: 'Kanyakumari, Kuzhithurai'
        }
      ]
    }
  },
   methods : {
    addEmployee(employee){
      const lastId = this.employees.length > 0 ? this.employees[this.employees.length - 1].id : 0;

      const id = lastId + 1;

      const newEmployee = {...employee, id}

      this.employees = [...this.employees, newEmployee];
    }
   }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

.parent-container {
  display: flex;
  flex-direction: column;
}

.small-container {
  margin-left: auto;
  margin-right: auto;
  margin-top: auto;
  margin-bottom: auto;
}
</style>
