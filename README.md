DESAFIO: CRUD de clientes 
Você deverá entregar um projeto Spring Boot contendo um CRUD completo de web services REST para
acessar um recurso de clientes, contendo as cinco operações básicas aprendidas no capítulo:<br>
-> Busca paginada de recursos <br>
-> Busca de recurso por id <br>
-> Inserir novo recurso <br>
-> Atualizar recurso <br>
-> Deletar recurso <br>
O projeto deverá estar com um ambiente de testes configurado acessando o banco de dados H2, deverá usar 
Maven como gerenciador de dependência, e Java como linguagem.
Um cliente possui nome, CPF, renda, data de nascimento, e quantidade de filhos. A especificação da 
entidade Client é mostrada a seguir (você deve seguir à risca os nomes de classe e atributos mostrados no 
diagrama): 

<img width="185" height="165" alt="image" src="https://github.com/user-attachments/assets/b565d396-7c51-4e40-8d38-23962563009d" />

Seu projeto deverá fazer um seed de pelo menos 10 clientes com dados SIGNIFICATIVOS (não é para 
usar dados sem significado como “Nome 1”, “Nome 2”, etc.). 
Seu projeto deverá tratar as seguintes exceções: 
. Id não encontrado (para GET por id, PUT e DELETE), retornando código 404. 
.Erro de validação, retornando código 422 e mensagens customizada para cada campo inválido. As 
regras de validação são: 
o Nome: não pode ser vazio 
o Data de nascimento: não pode ser data futura (dica: use @PastOrPresent)
<p>
Busca de cliente por id
GET /clients/1
</p>  
Busca paginada de clientes<br>
GET /clients?page=0&size=6&sort=name
<p>
  
Inserção de novo cliente<br>
POST /clients<br>
{<br>
 "name": "Maria Silva",<br>
 "cpf": "12345678901",<br>
 "income": 6500.0,<br>
 "birthDate": "1994-07-20",<br>
 "children": 2<br>
}
</p>  
<p>
Atualização de cliente<br>
PUT /clients/1<br>
{<br>
 "name": "Maria Silvaaa",<br>
 "cpf": "12345678901",<br>
 "income": 6500.0,<br>
 "birthDate": "1994-07-20",<br>
 "children": 2<br>
}
</p> 
<p>
Deleção de cliente
DELETE /clients/1
</p>
<p>
CHECKLIST: <br>
1. Busca por id retorna cliente existente <br>
2. Busca por id retorna 404 para cliente inexistente <br>
3. Busca paginada retorna listagem paginada corretamente <br>
4. Inserção de cliente insere cliente com dados válidos <br>
5. Inserção de cliente retorna 422 e mensagens customizadas com dados inválidos <br>
6. Atualização de cliente atualiza cliente com dados válidos <br>
7. Atualização de cliente retorna 404 para cliente inexistente <br>
8. Atualização de cliente retorna 422 e mensagens customizadas com dados inválidos <br>
9. Deleção de cliente deleta cliente existente <br>
10. Deleção de cliente retorna 404 para cliente inexistente
</p>
