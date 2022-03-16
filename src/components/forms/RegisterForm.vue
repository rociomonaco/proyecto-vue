<template>

    <section class="w-full max-w-xs">
        <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2"  for="name">
                    *Name
                </label>
                <input v-model="name" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="name" type="text" placeholder="Username">
            </div>
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2"  for="surname">
                    *Surname
                </label>
                <input v-model="surname" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="surname" type="text" placeholder="Username">
            </div>
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2"  for="username">
                    *UserName
                </label>
                <input v-model="username" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username">
            </div>
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="phone">
                    *Phone
                </label>
                <input v-model="phone"  class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="phone" type="text" placeholder="Username">
            </div>
            <div class="mb-6">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                    *Password
                </label>
                <input v-model="password"  class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
            </div>
            <div class="mb-6">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="passwordMatch">
                    *Confirm Password 
                </label>
                <input v-model="passwordMatch" class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="passwordMatch" type="password" placeholder="******************">
                <!-- msg password doesn´t match -->
                <p class="text-red-500 text-xs italic" v-if="(password != '' && passwordMatch != '') && (password != passwordMatch)">The password does not match.</p>
                <!--/ msg password doesn´t match -->
            </div>
            <div class="flex items-center justify-between">
                <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"  @click="validate" type="button">
                    Register
                </button>

            </div>
        </form>

        <!-- msg all fields are required -->
        <div v-if="go === false">
            <h3>All fields containing * are required.</h3>
        </div>
        <!-- msg all fields are required -->



        <!-- NOTE: Entrega form -->
        <table class="table-fixed" v-if="go">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Surname</th>
                    <th>UserName</th>
                    <th>Phone</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>{{name}}</td>
                    <td>{{surname}}</td>
                    <td>{{username}}</td>
                    <td>{{phone}}</td>
                </tr>
            </tbody>
        </table>

        
    </section>
  


</template>

<script>
export default {
    "name" : "RegisterForm", 
    data(){
        return{
            name : "",
            surname : "",
            username : "",
            phone: "",
            password : "",
            passwordMatch : "",
            go : ""
        }
    },
    "methods":{
        validate(){
            this.go = "";
            if(this.name != "" && this.surname != "" && this.phone != "" && this.password != "" && this.passwordMatch != "" ) {
                this.go = true;
            }else{
                return this.go = false;
            }
        }
        
    },
    computed:{

    }
}
</script>

<style>

</style>