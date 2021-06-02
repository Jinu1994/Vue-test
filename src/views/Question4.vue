<template>
    <div id="parent">
        <h5>Question 4</h5>
        <child2>
            <div slot="header">
                <p>Header Slot</p>
                <span>Testing multiple slots</span>
            </div>
            <div slot="body">
                <p>Body Slot</p>
                <span>Testing multiple slots</span>
            </div>
        </child2>
    </div>
</template>
<script>
import Child2 from '../components/Child2'
export default {
    components:{
        Child2
    }
}
</script>
