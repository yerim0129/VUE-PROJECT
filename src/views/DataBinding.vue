<template>
    <label for="">
        <input type="checkbox" value="서울" v-model="checked">{{ checked }}
    </label>

    <label for="">
        <input type="checkbox" value="부산" v-model="checked">{{ checked }}
    </label>

    <label for="">
        <input type="checkbox" value="광명" v-model="checked">{{ checked }}
    </label>

    <br>

    <span>체크한 지역 : {{ checked }}</span>
</template>
<script>

export default {
  name: 'DataBinding',
  data () {
    return {
        checked: []
  };
},
}
</script>
