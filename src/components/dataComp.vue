<template>
    <div>
        Resultado: {{getExtenso()}}     
    </div>
</template>

<script>

export default {
    props: {
      dataParam: String,
    },
    data() {
      return {
        mes: ['jan', 'fev', 'mar', 'abr', 'mai', 'jun',
        'jul', 'ago', 'set', 'out', 'nov', 'dez']
      }
    },
    methods: {
    getExtenso(){
      if (this.dataParam) {
        const d = this.dataParam.split('-')
        return d[2] + ' ' + this.mes[parseInt(d[1]-1)]
                    + ' ' + d[0]
      }
    return ""
    }
  }
}
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
