<script setup lang="ts">
const props = defineProps({
  visible: {
    type: Boolean,
    default: false,
  },
})

const emit = defineEmits([`close`])

function onUpdate(val: boolean) {
  if (!val) {
    emit(`close`)
  }
}
</script>

<template>
  <Dialog :open="props.visible" @update:open="onUpdate">
    <DialogContent>
      <DialogHeader>
        <DialogTitle>关于</DialogTitle>
      </DialogHeader>
      <div class="text-center">
        <h3>水木-信奥 公众号 Markdown 编辑器</h3>
        <p>使用上的问题，扫码咨询！</p>
        <img
          class="mx-auto my-5"
          src="https://oj.noicoding.cn/file/2/oDFtQ50DVK-VrSF18vDat.png"
          alt="水木-信奥 牛老师"
          style="width: 40%"
        >
      </div>
    </DialogContent>
  </Dialog>
</template>
