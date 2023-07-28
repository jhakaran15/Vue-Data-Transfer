<template>
    <div>
        <h3>Sibling Component</h3>
        <p>Message from child: {{ message }}</p>
    </div>
</template>
  
<script>
export default {
    props: {
        message: {
            type: String,
            default: "",
        },
    },
};
</script>  