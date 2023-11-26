<template>
    <div>
        <form v-on:submit.prevent="handledata">
            <div class="txtlabel">Employee name</div>
            <input class="textbox" type="text" placeholder="Employee Name" v-model="employee.name" />
            <div class="txtlabel">Employee Address</div>
            <input class="textbox" type="text" placeholder="Employee Address" v-model="employee.address" />
            <div>
                <button class="button3">Add Employee</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    name: 'employee-form',
    data() {
        return {
            employee: {
                name: '',
                address: ''
            }
        }
    },
    methods: {
        handledata() {
            this.$emit('add:employee', this.employee)
        }
    }
}
</script>

<style scoped>
.button3 {
    border-radius: 8px;
    height: 30px;
    width: 200px;
}

input[type=text] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}
</style>