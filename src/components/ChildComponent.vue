<template>
    <div>
        <h3>Child Component</h3>
        <input type="text" v-model="message" />
        <button @click="sendMessageToParent">Send Message to Parent</button>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            message: "",
        };
    },
    methods: {
        sendMessageToParent() {
            this.$emit("messageToParent", this.message);
        },
    },
};
</script>  