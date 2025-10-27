# Projeto 3: Controle de Chaves 🔑 
---
## O Cenário 👨‍💼


Parabéns\! Você acaba de ser contratado(a) como a nova pessoa desenvolvedora de uma pequena empresa. O ambiente é ótimo, mas alguns processos ainda são... digamos, "analógicos". O controle de quem está com cada chave das salas ainda é feito em um bloco de notas.

Sua primeira tarefa é criar um script Python simples que resolva isso, utilizando SQLite.

Seu chefe pediu o seguinte:

    "Crie um programa que guarde o nome do responsável e a sala correspondente. Por enquanto, só cadastre a Ana da 'Recepção', o Bruno do 'Financeiro' e a Carla do 'Depósito'. Depois, o programa precisa me dizer quem está com a chave do 'Depósito'."

## 📋 Sugestões e Requisitos da Missão

Seu chefe foi bem claro sobre o que o programa precisa fazer nesta primeira versão (o "Mínimo Viável"):

1.  **Criar o Banco de Dados:** O script deve criar um banco de dados. O nome pode ser `empresa.db`, por exemplo.
2.  **Modelar a Tabela:** Dentro do banco, pode haver uma tabela chamada `chaves` com as seguintes colunas:
      * `id` (Chave Primária, Inteiro, Autoincremento)
      * `sala` (Texto, não pode ser nulo)
      * `responsavel` (Texto, não pode ser nulo)
3.  **Povoamento Inicial:** O programa pode inserir os seguintes registros na tabela (apenas uma vez\!):
      * Sala: `Recepção`, Responsável: `Ana`
      * Sala: `Financeiro`, Responsável: `Bruno`
      * Sala: `Depósito`, Responsável: `Carla`
4.  **Consulta Específica:** O programa precisa ter uma função que busca e exibe no console quem é o responsável pela chave do `'Depósito'`.
5.  **Resultado Final:** Ao executar o script, ou a query, a saída esperada no terminal pode ser algo como:
    ```
    A chave da sala 'Depósito' está com: Carla
    ```

## 💡 Roteiro Sugerido para o Sucesso

Se não souber por onde começar, siga estes passos:

1.  **Importe a biblioteca `sqlite3`**.
2.  **Crie a conexão** com o arquivo do banco de dados (`empresa.db` ou o nome que você escolher).
3.  **Crie um cursor**. É ele quem executa os comandos SQL.
4.  **Escreva o comando SQL** para criar a tabela `chaves` (dica: use `CREATE TABLE IF NOT EXISTS` para evitar erros ao rodar o script várias vezes).
5.  **Execute o comando** de criação da tabela.
6.  **Insira os três registros iniciais**. Lembre-se de usar `conn.commit()` para salvar as alterações\!
7.  **Escreva e execute o `SELECT`** para buscar o responsável pela sala informada. Use `WHERE` para filtrar.

Boa sorte, dev\! O futuro da organização da empresa está em suas mãos. 💪