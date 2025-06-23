<script setup lang="ts">
import { computed } from 'vue'
import { cn } from "../../lib/utils"

interface Props {
  modelValue: string
  type?: string
  class?: string
}

const props = defineProps<Props>()
const emit = defineEmits<{
  (e: 'update:modelValue', value: string): void
}>()

function onInput(event: Event) {
  const target = event.target as HTMLInputElement
  emit('update:modelValue', target.value)
}

const inputClass = computed(() =>
  cn(
    'flex h-10 w-full rounded-md border border-input bg-background px-3 py-2 text-base ring-offset-background file:border-0 file:bg-transparent file:text-sm file:font-medium file:text-foreground placeholder:text-muted-foreground focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 md:text-sm',
    props.class
  )
)
</script>

<template>
  <input
    :type="props.type || 'text'"
    v-bind="$attrs"
    :class="inputClass"
    :value="props.modelValue"
    @input="onInput"
  />
</template>
