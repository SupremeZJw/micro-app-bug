<script setup>
import { onMounted, reactive, ref, watch } from 'vue';

defineOptions({
  name: 'CreateForm'
});

const emit = defineEmits(['onCancel']);

const onCancel = () => {
  emit('onCancel')
}
</script>

<template>
  <a-modal open title="Basic Modal" @ok="onCancel" @cancel="onCancel">
    <div class="flex">
      <div class="mr-0 flex-1">
        <div class="top-approval">
          <span>审批意见:</span>
          <div class="flex-1">
            <AInput class="w-60%" placeholder="请输入" />
          </div>
          <AButton type="primary">同意</AButton>
          <AButton type="primary" danger>驳回</AButton>
        </div>
        <AInput />
      </div>
    </div>
  </a-modal>
</template>

<style scoped>
.top-approval {
  padding: 12px 24px;
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 8px;
  --uno: bg-primary-100;
}

.title-box {
  padding: 12px 24px;
  border-bottom: 4px solid #f0f2f5;
  font-weight: bold;
}

.form-box {
  padding: 24px 24px 12px;
}

.tabs-box {
  padding: 12px 24px;
}

.buttons {
  margin-top: 20px;
  display: flex;
  justify-content: end;
  gap: 20px;
}

.approval-info {
  width: 300px;
  position: relative;

 
}

.info-title-box {
    width: 100%;
    padding: 12px 24px;
    font-size: 20px;
    font-weight: bold;
  }

  .infos {
    padding: 12px 24px;
    display: flex;
    flex-direction: column;


  }

  .info-status {
      margin: 8px 0;
    }

    .info-user {
      padding: 2px 8px;
      margin: 4px 0 12px 30px;
      border: 1px solid rgba(0, 0, 0, 0.25);
      font-size: 10px;
      color: #333333;
      background-color: rgba(242, 242, 242, 1);
      box-sizing: border-box;
      border-width: 1px;
      border-style: solid;
      border-color: rgba(170, 170, 170, 1);
      border-radius: 81px;
    }

    .info-time {
      margin: 4px 0;
      margin-left: 30px;
      font-weight: 400;
      font-style: normal;
      font-size: 12px;
      color: rgba(0, 0, 0, 0.4470588235294118);
    }

.base-bg {
  background: rgba(22, 155, 213, 0.074);
}

:deep(.ant-form .ant-motion-collapse) {
  overflow: visible;
}
</style>
