<template>
    <div>
        <el-cascader
            size="large"
            :options="regionData"
            v-model="selectedOptions">
        </el-cascader>
    </div>
    <div>
        <input type="date" v-model="selectedBirthday" />
    </div>
    <div>
        <select v-model="selectedSex">
            <option>male</option>
            <option>female</option>
        </select>
    </div>
    <div>
        <button @click="getId">submit</button>
    </div>
    <div>
        <p>{{id}}</p>
    </div>

</template>

<script>
import { regionData } from 'element-china-area-data'
import axios from 'axios'


export default {
    name: 'InformationChoose',
    data () {
        return {
            regionData,
            selectedOptions: [],
            selectedBirthday: this.value,
            selectedSex: "male",
            id: ""
        }
    },
    methods: {
        getId() {
            axios.post("http://127.0.0.1:5000/id", {
                area: this.selectedOptions[2],
                birthday: this.selectedBirthday,
                male: this.selectedSex
            }).then(response => {
                this.id = response.data.id
            }).catch(error => {
                console.error(error)
            })
        }
    }
}
</script>