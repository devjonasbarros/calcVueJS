<script >

export default{
    data(){
        return{ 
        num1: '',
        num2: '',
        selected: '',
        Aritmetica: 0
        }
    },
    methods:{
        getAdicao(){
        return this.num1 + this.num2;
        },
        getSubtrair(){
            return this.num1 - this.num2;
        },
        getMultiplicar(){
            return this.num1 * this.num2;
        },
        getDividir(){
            return this.num1 / this.num2;
        },
        getLimpar(){
            return this.num1, this.num2 = ''
        }
    }
    }

</script>

<template>
<div id="app">

    <header class="p-5 mb-4 bg-light rounded-6">
    <h2 >CALCULADORA ARIT...</h2> <br> <br>

    <input type="number" placeholder=" Valor I" v-model="num1"> <br> <br>
    <input type="number" placeholder=" Valor II" v-model="num2">

    
<select v-model="selected">
  <option disabled value="">Operador</option>
  <option value="1">Adição</option>
  <option value="2">Subtrair</option>
  <option value="3">Multiplicar</option>
  <option value="4">Dividir</option>

</select>
<br>

</header>

<div class="resultado">
    <p>Primeiro numero informado foi: {{ num1 }}</p>
    <p>O segundo numero informado é: {{ num2 }}</p>
    
</div>

    <div v-if="selected == 1">
        <h1> {{ getAdicao() }} </h1>
    </div>

    <div v-else-if="selected == 2">
        <h1>      {{ getSubtrair() }}    </h1>
    </div>

    <div v-else-if="selected == 3">
        <h1>        {{ getMultiplicar() }}
        </h1>
    </div>

    <div v-else-if="selected == 4">
        <h1>         {{ getDividir() }}
        </h1>
    </div>


</div>

</template>


<style scoped>

#{
    width: 300px;
    height: 300px;
    background-color: black;
}

input{
    width: 180px;
    height: 32px;
    font-size: 22px;
}

select{
    width: 120px;
    height: 32px;
    margin-left: 10px;
    border-radius: 30px;
    padding-left: 5px;
    color: blue;
    font-size: 16px;

}


</style>
