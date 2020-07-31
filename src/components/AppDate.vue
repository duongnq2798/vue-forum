<template>
  <div>
    <div :title="timestamp | humanFriendlyDate">
      {{timestamp | diffForHumans}}
    </div>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  props: {
    timestamp: {
      required: true,
      type: Number
    }
  },
  filters: {
    humanFriendlyDate (data) {
      return moment.unix(data).format('MMMM Do YYYY, h:mm:ss a')
    },

    diffForHumans (data) {
      return moment.unix(data).fromNow()
    }
  }
}
</script>