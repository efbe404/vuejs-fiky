<template>
<header>
  <h1>Tugas 2</h1>
</header>

<main>
<table>
  <tr>
    <td>
      <h2>{{judul}}</h2>
      <p>a = {{a}}</p>
      <p>b = {{b}}</p>
      <p>Maka Luas segitiganya: {{luasSegitigaStatic}}</p>
    </td>
  </tr>
  <tr>
    <td>
      <h2>{{judul2}}</h2>
      <p>Alas : <input type="text" name="Alas" placeholder="Alas" v-model="alasDinamis "></p>
      <p>Tinggi : <input type="text" name="tinggi" placeholder="Tinggi" v-model="tinggiDinamis "></p>
      <p>Menghitung Luas Segitiga:<br>
        Alas: {{alasDinamis}}<br>
        Tinggi : {{tinggiDinamis}}<br>
        Luas segitiga: {{luasSegitiga}}</p>
    </td>
  </tr>
</table>
</main>

</template>
<script>


export default {
  name: 'App',
  data(){
    return{
      judul: "Menghitung Luas Segitiga Static",
      a: 10,
      b: 20,
      judul2: "Menghitung luas segitiga Dynamic",
      alasDinamis:"",
      tinggiDinamis:""
    }
  },
  computed:{
    luasSegitigaStatic(){
      return (this.a*this.b)/2;
    },
    luasSegitiga(){
      if(this.alasDinamis=="" && this.tinggiDinamis==""){
          return "";
      }else{
      return (this.alasDinamis*this.tinggiDinamis)/2;
      }
    }
  }
}
</script>
<style scoped>
table, td, tr{
  border: 1px solid black;
  text-align: left;
}
</style>