<template>
    <div>
        <p>this is my result counter {{ doubleCounter }}</p>
        <p>Number of clicks: {{ counterClicks }}</p>
    </div>
</template>

<script>
//import {mapState, mapMutations, mapGetters, mapActions} from "vuex";
import { mapGetters } from "vuex";
export default {
    name: "resultCounter",
    computed: {
        // counter: function() {
        //    return this.$store.getters.doubleCounter;
        // },
        // clicks: function () {
        //     return this.$store.getters.counterClicks;
        // }
        //...mapActions([]),
        ...mapGetters(['doubleCounter', 'counterClicks'])
    }
}
</script>