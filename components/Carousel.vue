<script setup lang="ts">
import { PropType, computed, onMounted, onUnmounted, ref } from 'vue';

const props = defineProps({
  sources: {
    type: Array as PropType<string[]>,
    required: true,
  },
  interval: {
    type: Number,
    default: 2000,
  },
  width: {
    type: String,
    default: '16rem',
  },
})

const total = computed(() => props.sources.length)
const current = ref(0)
const hovered = ref(false)
const popover = ref(false)
const active = ref<number>(NaN)

const intervalId = ref(0)
onMounted(() => {
  intervalId.value = setInterval(() => {
    if (hovered.value || popover.value) return
    current.value = (current.value + 1) % total.value
  }, props.interval)
})
onUnmounted(() => clearInterval(intervalId.value))
</script>

<template>
  <TransitionGroup relative overflow-x-hidden h-200 :style="{ width }" name="fade" tag="div"
    @mouseover="hovered = true" @mouseleave="hovered = false" v-bind="$attrs">
    <template v-for="src, i in sources" :key="src">
      <img v-show="i === current" absolute left-0 top-0 :style="{ width }" :src="src"
        @click="popover = true, active = i" />
    </template>
  </TransitionGroup>
  <div fixed z-1 flex items-center justify-center backdrop-blur transition-all duration-300
    :class="popover ? 'inset-0' : 'hidden op0 inset-[50%]'">
    <img w-full h-full object-contain :src="sources[active]" @click="popover = false" />
  </div>
</template>
