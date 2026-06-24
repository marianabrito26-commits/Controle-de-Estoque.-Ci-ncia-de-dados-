(# Controle-de-Estoque.-Ci-ncia-de-dados-
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Controle de Estoque</title>
  <style>
    body{
      font-family: Arial;
      margin:20px;
      background: #f4f4f4;
  }
  h1{
    text-align: center;
  }
  
  .container {  
   background: white;
   padding:20px;
   max-width: 600px;
   margin: auto;
   border-radius: 10px
   box shadow: 0 0 10px #ccc;
 }

 input{ 
   padding: 8px;
   margin: 5px;
   widht: calc(100%-20px);
}

button {
  padding: 10px;
  background: green;
  color: white;
  border: none;
  cursor: pointer; 
  width: 100%;
  margin-top: 10px;
}

table {
  width: 100%;
  margin-top: 10px;
}

table,th,td {
  border: 1px solid #ccc
  text-align: center;
}

th,td {
  padding: 10px
}

.delete {
 background: red;
 padding: 5px;
 color: white;
 cursor: pointer;
 border: none;
}
  </style>
</head>
</body>

<div class="container">
 <h1>ControledeEstoque</h1>

 <input type="text" id="produto" placeholder="Nome do produto">
 <input type="number" id="quantidade" placeholder="Quantidade">

 <button onclick="adicionarProduto()">Adicionar Produto</button>

 <table>
   <thead>
     <tr>
       <th>Produto</th>
       <th>Quantidade</th>
       <th>Ação</th>
     </tr>
   </thead>
   <tbody id="tabelaEstoque"></tbody>
 </table>
</div>

<script>
  let estoque = JSON.parse(localStorage.getItem("estoque")) || [];

  function salvar() {
    localStorage.setItem("estoque", JSON.stringify(estoque));
  }
  /script>
