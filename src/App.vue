<script setup>
import { ref } from 'vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmacaosenha = ref('')
const datadenascimento = ref('')
const enderecorua = ref('')
const endereconumero = ref('')
const enderecobairro = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref([])
const linguagem = ref([])
const biografia = ref('')


const novaLinguagem = ref('')
const novoHobbie = ref('')

const aparecer = ref(false)

function validacao() {
if( confirmacaosenha.value != senha.value) {
  alert("Confirmação de senha invalida")

} 
else { aparecer.value = !aparecer.value }
}

if( nome.value == '' || email.value == ''  senha.value == '' || confirmacaosenha.value == ''  datadenascimento.value == '' || enderecobairro.value == ''  enderecorua.value == '' || endereconumero.value == '' )



</script>

<template>
  <div id="editar">
    <div>
      <div class="nome">
        <input type="text" v-model="nome" placeholder="digite seu nome :">
      </div>
      <div class="email">
        <input type="email" v-model="email" placeholder="digite seu email :" />
      </div>
      <div class="senha">
        <input type="password" v-model="senha" placeholder="digite sua senha :" />
      </div>
      <div class="confirmação_senha">
        <input type="password" v-model="confirmacaosenha" placeholder="confirmação da senha :" />
      </div>
      <div class="data">
        <input type="date" v-model="datadenascimento" placeholder="digite sua data de nascimento :" />
      </div>
      <div class="rua">
        <input type="text" v-model="enderecorua" placeholder="digite sua rua :" />
      </div>
      <div class="numero_rua">
        <input type="number" v-model="endereconumero" placeholder="digite o numero da sua rua :" />
      </div>
      <div class="bairro">
        <input type="text" v-model="enderecobairro" placeholder="diga o seu bairro :" />
      </div>
      <div class="cidade">
        <input type="text" v-model="cidade" placeholder="digite a sua cidade :" />
      </div>
      <div class="estado">
        <h4>insira seu estado :</h4>
        <select v-model="estado">
          <option value="AC">Acre</option>
          <option value="AL">Alagoas</option>
          <option value="AP">Amapa</option>
          <option value="AM">Amazonas</option>
          <option value="BA">Bahia</option>
          <option value="CE">Ceara</option>
          <option value="DF">Distrito Federal</option>
          <option value="ES">Espirito Santo</option>
          <option value="GO">Goias</option>
          <option value="MA">Maranhão</option>
          <option value="MT">Mato Grosso</option>
          <option value="MS">Mato Grosso Do Sul</option>
          <option value="MG">Minas Gerais</option>
          <option value="PA">Para</option>
          <option value="PB">Paraiba</option>
          <option value="PR">Parana</option>
          <option value="PE">Pernanbuco</option>
          <option value="PI">Piaui</option>
          <option value="RJ">Rio De Janeiro</option>
          <option value="RN">Rio Grande do Norte</option>
          <option value="RS">Rio Grande Do Sul</option>
          <option value="RO">Rondonia</option>
          <option value="RR">Roraima</option>
          <option value="SC">Santa Catarina</option>
          <option value="SP">São Paulo</option>
          <option value="SE">Sergipe</option>
          <option value="TO">Tocantins</option>
        </select>
      </div>
      <div class="hobbies"><input type="text" v-model="novoHobbie" @keypress.enter="hobbies.push(novoHobbie); novoHobbie = ''" placeholder="digite seus hobbies :" /></div>

      <div class="linguagem">
        <input type="text" v-model="novaLinguagem" @keypress.enter="linguagem.push(novaLinguagem); novaLinguagem = ''" placeholder="digite a linguagem da programação :" />
      </div>
      <div class="biografia">
        <input type="text" v-model="biografia" placeholder="digite sua biografia :" />
      </div>
      <button type="submit" @click="validacao"> enviar</button>
    </div>

  </div>
  <div id="resposta" v-if="aparecer">
    <h1>Perfil depois de atualizado :</h1>
    <div class="nome_novo">
      <p>{{ nome }}</p>
    </div>
    <div class="data_nascimento_nova">
      <p>{{ datadenascimento }}</p>
    </div>
    <div class="email_novo">
      <p>{{ email }}</p>
    </div>
    <div class="senha_novo"></div>
    <div class="endereco_atual">
      <p>
        Endereço: {{ enderecorua }}, {{ endereconumero }},{{ enderecobairro }}, {{ cidade }},
        {{ estado }}
      </p>
    </div>
    <div class="hoobie_novo">Hoobie(s): {{ hobbies.join(", ") }}</div>
    <div class="linguagem_nova">Linguagem(s) de Programação: {{ linguagem.join(", ") }}</div>
    <div class="bio_nova">Biografia: {{ biografia }}</div>
    <button type="submit" @click="validacao"> Editar</button>

  </div>
</template>

<style>
div {
  margin: 3px;
}

#editar {
  background-color: blueviolet;
  border-radius: 5%;
  border-color: rgb(28, 224, 21);
  border-style: groove;
  padding: 12px;
  box-shadow: 3px 4px 15px black;
}

#resposta {
  background-color: rgb(255, 52, 52);
  border-radius: 5%;
  border-color: rgb(255, 229, 62);
  border-style: groove;
  padding: 12px;
  box-shadow: 3px 4px 15px rgb(0, 0, 0);
}</style>