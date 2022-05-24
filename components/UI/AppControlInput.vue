<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-12">
        <label> <slot /> </label>
      </div>
    </div>
    <div class="row">
      <div class="col-xl-12">
        <input
        style="width: 100%"
          v-if="controlType === 'input'"
          v-bind="$attrs"
          :value="value"
          @input="$emit('input', $event.target.value)"
        />
      </div>
    </div>
    <div class="row">
      <div class="col-xl-12">
        <textarea
        style="width: 100%"
        v-if="controlType === 'textarea'"
        rows="10"
        :value="value"
        @input="$emit('input', $event.target.value)"
        >
        </textarea>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppInputControl',
  props: {
    controlType: {
      type: String,
      default: 'input'
    },
    value: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
.input-control {
  margin: 10px 0;
}

.input-control label {
  display: block;
  font-weight: bold;
}

.input-control input,
.input-control textarea {
  display: block;
  width: 100%;
  box-sizing: border-box;
  font: inherit;
  border: 1px solid #ccc;
  padding: 5px;
}

.input-control input:focus,
.input-control textarea:focus {
  background-color: #eee;
  outline: none;
}
</style>
