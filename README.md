[![Netlify Status](https://api.netlify.com/api/v1/badges/d9027ab6-12ce-4786-8082-da9e7ee942f4/deploy-status)](https://app.netlify.com/sites/cadastrojscrud/deploys)
# CRUD em JavaScript, CSS e HTML

Neste projeto, desenvolvi um CRUD simples utilizando apenas JavaScript puro, CSS e HTML. O objetivo principal era criar um CRUD (Create, Read, Update, Delete) que permite a criação, leitura, atualização e exclusão de registros de uma lista.

## Sobre o Projeto

Este é um projeto básico de demonstração das minhas habilidades em programação utilizando JavaScript. O CRUD permite que o usuário realize as seguintes operações:

- **Criar**: Adicionar um novo item à lista.
- **Ler**: Visualizar a lista de itens existentes.
- **Atualizar**: Editar os detalhes de um item existente.
- **Excluir**: Remover um item da lista.

## Objetivos Futuros

Este projeto servirá como base para incorporar funcionalidades semelhantes em projetos maiores e mais complexos. Planejo explorar outras tecnologias e frameworks para aprimorar a interface e a experiência do usuário.

### Como funciona o C.R.U.D. 

- Vou explicar cada parte do código passo a passo de uma maneira simples:

1. **Selecionando Elementos do HTML:**

   ```javascript
   const modal = document.querySelector('.modal-container')
   const tbody = document.querySelector('tbody')
   const sNome = document.querySelector('#m-nome')
   const sFuncao = document.querySelector('#m-funcao')
   const sSalario = document.querySelector('#m-salario')
   const btnSalvar = document.querySelector('#btnSalvar')
   ```

   Essas linhas estão selecionando elementos do HTML por meio de seletores (como classes ou IDs) e os armazenando em variáveis para serem usados posteriormente no código.

2. **Função `openModal()`:**

   ```javascript
   function openModal(edit = false, index = 0) {
     // Código para abrir o modal e detectar o clique fora do modal
     if (edit) {
       // Preenche os campos do modal com os valores do item selecionado para edição
     } else {
       // Limpa os campos do modal
     }
   }
   ```

   A função `openModal()` controla a abertura do modal. Se `edit` for verdadeiro, preenche os campos do modal com os valores do item selecionado para edição; caso contrário, limpa os campos.

3. **Função `editItem()` e `deleteItem()`:**

   ```javascript
   function editItem(index) {
     openModal(true, index)
   }

   function deleteItem(index) {
     // Remove o item da lista e atualiza o armazenamento
     // Recarrega a lista de itens
   }
   ```

   Essas funções são chamadas quando os botões de edição e exclusão são clicados. `editItem()` chama `openModal()` para editar o item, e `deleteItem()` remove o item selecionado da lista.

4. **Função `insertItem()` e Manipulação do DOM:**

   ```javascript
   function insertItem(item, index) {
     // Cria uma nova linha na tabela com os detalhes do item
     // Insere botões de edição e exclusão
   }
   ```

   A função `insertItem()` cria uma nova linha na tabela (`<tr>`) e insere os detalhes do item e botões de edição e exclusão.

5. **Evento de Clique no Botão "Salvar":**

   ```javascript
   btnSalvar.onclick = e => {
     // Verifica se os campos estão preenchidos
     // Atualiza os dados do item editado ou insere um novo item
     // Fecha o modal, recarrega a lista de itens e reseta o ID
   }
   ```

   Esta parte do código manipula o evento de clique no botão "Salvar". Ele verifica se os campos estão preenchidos, atualiza os dados do item editado ou insere um novo item na lista e, em seguida, fecha o modal, recarrega a lista de itens e reseta o ID.

6. **Função `loadItens()`:**

   ```javascript
   function loadItens() {
     // Carrega itens do armazenamento e insere cada item na tabela
   }
   ```

   A função `loadItens()` carrega os itens armazenados e insere cada item na tabela por meio da função `insertItem()`.

7. **Funções de Armazenamento - `getItensBD()` e `setItensBD()`:**

   ```javascript
   const getItensBD = () => JSON.parse(localStorage.getItem('dbfunc')) ?? []
   const setItensBD = () => localStorage.setItem('dbfunc', JSON.stringify(itens))
   ```

   Essas funções são usadas para obter e definir os itens no armazenamento local do navegador.

8. **Chamada Inicial para Carregar Itens:**

   ```javascript
   loadItens()
   ```

   No final do código, a função `loadItens()` é chamada para carregar os itens na página quando ela é carregada.

## Como Executar o Projeto

1. Clone este repositório para o seu ambiente local.
2. Abra o arquivo `index.html` em um navegador da web.
3. Interaja com o CRUD usando os botões e campos fornecidos na página.

## Tecnologias Utilizadas

- JavaScript: Lógica e interatividade do CRUD.
- CSS: Estilização e layout da interface.
- HTML: Estrutura da página.

## Finalidade

Este projeto foi criado para fins de aprendizado.

## Contato

Se você quiser entrar em contato para discutir ideias, compartilhar experiências ou colaborar em projetos, sinta-se à vontade para me contatar através do meu [LinkedIn](https://www.linkedin.com/in/robson-ferreira-508247134/).

