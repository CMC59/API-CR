<template>
  <div>
    
  </div>
</template>

<script>
  const headers = {'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiIsImtpZCI6IjI4YTMxOGY3LTAwMDAtYTFlYi03ZmExLTJjNzQzM2M2Y2NhNSJ9.eyJpc3MiOiJzdXBlcmNlbGwiLCJhdWQiOiJzdXBlcmNlbGw6Z2FtZWFwaSIsImp0aSI6ImIxNTI5ZDU4LWU2OTctNDUwMy05NTdlLTZjZGY4MTg4YzE5ZCIsImlhdCI6MTY2MDE2MDc3OCwic3ViIjoiZGV2ZWxvcGVyLzAzZTE3MDc2LWI3M2YtZTY2ZS01ZDdmLTEwODJkNjU1NWUzZiIsInNjb3BlcyI6WyJyb3lhbGUiXSwibGltaXRzIjpbeyJ0aWVyIjoiZGV2ZWxvcGVyL3NpbHZlciIsInR5cGUiOiJ0aHJvdHRsaW5nIn0seyJjaWRycyI6WyI4Mi42Ni4xMDIuNTUiXSwidHlwZSI6ImNsaWVudCJ9XX0.8s_Buve-b6pTN4puVSYTacJNMDp-hrUT_WuQYqRx5ZuaXscTEN0KtDSGTHMdKw3nrSuHO-WPELgAZmnnckhrXQ'}
  export default {
    data() {
      return {
        playerInfos: null,
        playerTag: '#RVUYGV2J0'
      }
    },
    methods: {
      async getPlayerInfos() {
        const transformedPlayerTag = encodeURIComponent(this.playerTag)
        console.log(transformedPlayerTag);
        this.playerInfos = await this.$axios.$get(`/api/players/${transformedPlayerTag}`, {headers})
      }
    },
    mounted() {
      this.getPlayerInfos()
    }
  }
</script>