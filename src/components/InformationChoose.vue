<template>
    <div id="app">
        <el-cascader
            size="large"
            :options="regionData"
            v-model="selectedOptions">
        </el-cascader>
    </div>
</template>

<script>
import { regionData } from 'element-china-area-data'

export default {
    name: 'InformationChoose',
    data () {
        return {
            regionData,
            selectedOptions: []
        }
    },
}
</script>