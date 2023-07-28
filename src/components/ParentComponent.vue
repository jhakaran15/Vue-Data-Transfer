<template>
  <div>
    <h2>Parent Component</h2>
    <p>Message from child: {{ messageFromChild }}</p>
    <p>Message from sibling: {{ messageFromSibling }}</p>
    <ChildComponent @messageToParent="handleMessageFromChild" />
    <SiblingComponent
      :message="messageFromChild"
      @messageToSibling="handleMessageFromSibling"
    />
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";
import SiblingComponent from "./SiblingComponent.vue";

export default {
  components: {
    ChildComponent,
    SiblingComponent,
  },
  data() {
    return {
      messageFromChild: "",
      messageFromSibling: "",
    };
  },
  methods: {
    handleMessageFromChild(message) {
      this.messageFromChild = message;
    },
    handleMessageFromSibling(message) {
      this.messageFromSibling = message;
    },
  },
};
</script>
