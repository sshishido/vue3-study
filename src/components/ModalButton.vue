<template>
  <button @click="state.modalOpen = true">
    Open full screen modal! (With teleport!)
  </button>
  <teleport to="#teleport-target">
    <div v-if="state.modalOpen" class="modal">
      <div>
        I'm a teleported modal! (My parent is "teleport-target")
        <button @click="state.modalOpen = false">
          Close
        </button>
      </div>
    </div>
  </teleport>
</template>

<script>
import { defineComponent, reactive } from "vue";

export default defineComponent({
  name: "Teleport",
  setup() {
    const state = reactive({
      modalOpen: false,
    });

    return { state };
  },
});
</script>

<style scoped>
.modal {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.modal div {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: white;
  width: 300px;
  height: 300px;
  padding: 5px;
}
</style>
