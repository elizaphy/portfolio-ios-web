<script setup lang="ts">
import { cn } from  "../../lib/utils"
import { ref, defineProps, defineEmits, computed } from 'vue'

const props = defineProps({
  modelValue: String,
  class: String,
  // Add other native textarea attributes if needed
  placeholder: String,
  disabled: Boolean,
  rows: String,
})

const emit = defineEmits(['update:modelValue'])

const inputRef = ref<HTMLTextAreaElement | null>(null)

const computedClass = computed(() =>
  cn(
    'flex min-h-[80px] w-full rounded-md border border-input bg-background px-3 py-2 text-sm ring-offset-background placeholder:text-muted-foreground focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50',
    props.class
  )
)

function updateValue(event: Event) {
  const target = event.target as HTMLTextAreaElement
  emit('update:modelValue', target.value)
}
</script>

<template>
  <textarea
    ref="inputRef"
    :class="computedClass"
    :placeholder="props.placeholder"
    :disabled="props.disabled"
    :rows="props.rows"
    :value="props.modelValue"
    @input="updateValue"
  />
</template>
