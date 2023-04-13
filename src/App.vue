<script>
import { ref } from 'vue'


const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmacaosenha = ref('')
const datadenascimento= ref('')
const enderecorua = ref('')
const endereconumero = ref('')
const enderecobairro = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagem = ref('')
const biografia = ref('')


</script>

<template>
<div class="nome"></div>
<div><input type="text" v-model="nome" placeholder="digite seu nome :"></div>
<div class="email"></div>
<div><input type="email" v-model="email" placeholder="digite seu email :"/></div>
<div class="senha"></div>
<div><input type="password" v-model="senha" placeholder="digite sua senha :"/></div>
<div class="confirmação_senha"></div>
<div><input type="password" v-model="confirmacaosenha" placeholder="confirmação da senha :"/></div>
<div class="data"></div>
<div><input type="date" v-model="datadenascimento" placeholder="digite sua data de nascimento :"/></div>
<div class="rua"></div>
<div><input type="text" v-model="enderecorua" placeholder="digite sua rua :"/></div>
<div class="numero_rua"></div>
<div><input type="number" v-model="endereconumero" placeholder="digite o numero da sua rua :"/></div>
<div class="bairro"></div>
<div><input type="text" v-model="enderecobairro" placeholder="diga o seu bairro :"/></div>
<div class="cidade"></div>
<div><input type="text" v-model="cidade" placeholder="digite a sua cidade :"/></div>
<div class = "estado">
<h4>insira seu estado :</h4>
<select v-model="estado">
<option value = "AC">Acre</option>
<option value = "AL">Alagoas</option>
<option value = "AP">Amapa</option>
<option value = "AM">Amazonas</option>
<option value = "BA">Bahia</option>
<option value = "CE">Ceara</option>
<option value = "DF">Distrito Federal</option>
<option value = "ES">Espirito Santo</option>
<option value = "GO">Goias</option>
<option value = "MA">Maranhão</option>
<option value = "MT">Mato Grosso</option>
<option value = "MS">Mato Grosso Do Sul</option>
<option value = "MG">Minas Gerais</option>
<option value = "PA">Para</option>
<option value = "PB">Paraiba</option>
<option value = "PR">Parana</option>
<option value = "PE">Pernanbuco</option>
<option value = "PI">Piaui</option>
<option value = "RJ">Rio De Janeiro</option>
<option value = "RN">Rio Grande do Norte</option>
<option value = "RS">Rio Grande Do Sul</option>
<option value = "RO">Rondonia</option>
<option value = "RR">Roraima</option>
<option value = "SC">Santa Catarina</option>
<option value = "SP">São Paulo</option>
<option value = "SE">Sergipe</option>
<option value = "TO">Tocantins</option>
</select></div>
<div class="hobbies"><div><input type="text" v-model="hobbies" placeholder="digite seus hobbies :"/></div></div>

<div class="linguagem"> </div>
<div><input type="text" v-model="linguagem" placeholder="digite a linguagem da programação :"/></div>
<div class="biografia"></div>
<div><input type="text" v-model="biografia" placeholder="digite sua biografia :"/></div>




</template>

<style>
div{
  margin: 3px;
}

</style>
