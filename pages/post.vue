<template>
    <h3 class="text-center mt-3 text-primary">Enter User Details</h3>
    <div class="d-flex justify-content-center mt-3 ">
        <form class="col-3 d-flex flex-column border border-primary rounded p-3">
            <div class="mb-3">
                <label for="exampleInputName" class="form-label">Name</label>
                <input type="name" v-model="name" class="form-control" id="exampleInputName"
                    aria-describedby="emailHelp" />
                <div id="nameHelp" class="form-text">
                    We'll never share your name with anyone else.
                </div>
            </div>
            <div class="mb-3">
                <label for="exampleInputEmail1" class="form-label">Age</label>
                <input type="number" v-model="age" class="form-control" id="exampleInputEmail1"
                    aria-describedby="emailHelp" />
                <div id="emailHelp" class="form-text">
                   Minimum Age 18
                </div>
            </div>
            <div class="mb-3">
                <label for="exampleInputPassword1" class="form-label">Gender</label>
                <input type="gender" v-model="gender" class="form-control" id="exampleInputPassword1" />
            </div>
            <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" id="exampleCheck1" />
                <label class="form-check-label" for="exampleCheck1">Check me out</label>
            </div>
            <button type="submit" @click.prevent="addUser" class="btn btn-primary">
                Submit
            </button>
        </form>
    </div>
</template>

<script>
import axios from "axios";
export default {
    data() {
        return {
            name: "",
            age: "",
            gender: "",
        };
    },
    methods: {
        async addUser() {
            let result = await axios.post("http://localhost:3001/student", {
                name: this.name,
                age: this.age,
                gender: this.gender,
            });
            console.warn(result);
        },
    },
};
</script>
