<template>
  <div>
    <h1>{{part.title}}</h1>
  </div>
  <div>
    {{part.description}}
  </div>
</template>

<script>
import parts from '../data/parts';

export default {
  name: 'PartInfo',
  computed: {
    part() {
      const { partType, id } = this.$route.params;
      return parts[partType].find((part) => part.id === +id);
    },
  },
};
</script>
