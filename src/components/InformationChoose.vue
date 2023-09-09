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
        <p> {{selectedBirthday}} </p>
    </div>
    <div>
        <select v-model="selectedSex">
            <option>male</option>
            <option>female</option>
        </select>
        <p>{{selectedSex}}</p>
    </div>
    <div>
        <button>submit</button>
    </div>

</template>

<script>
import { regionData } from 'element-china-area-data'

export default {
    name: 'InformationChoose',
    data () {
        return {
            regionData,
            selectedOptions: [],
            selectedBirthday: this.value,
            selectedSex: "male"
        }
    }
}
</script>