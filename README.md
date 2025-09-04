## ⚙️ Instalação

1. Realize o clone do repositório:
```
git clone https://github.com/FThiagoB/Capacita-Brasil-MAO2-Cadastro-de-Alunos.git
cd Capacita-Brasil-MAO2-Cadastro-de-Alunos
```

2. Instale os módulos:
```
npm install

```

3. Configure o arquivo .env com a URL de conexão do banco de dados (PostgreSQL):
```
DATABASE_URL="postgresql://usuario:senha@localhost:5432/fsn3?schema=public"
```

4. Use o comando migrate do Prisma:
```
npx prisma migrate dev --name init
```

4. Use o comando de seed para popular a tabela com dados de exemplo:
```
npm run seed
```

5. Inicie o servidor:
```
npm run start
```

## 🗺️ Rotas e funcionalidades
Foi criado uma **API RESTFul** que implementa as operações de **CRUD** (*Create*, *Read*, *Update* e *Delete*) usando o **Prisma ORM**.

| Método | Rota | Descrição |
| :------: | :---------: | :-----: |
| GET   | http://localhost:3000/alunos | Retorna uma resposta JSON com as informações de todos os alunos do banco de dados. |
| POST  | http://localhost:3000/alunos | Realiza o cadastro de um aluno ao passar as informações necessárias no corpo da requisição (formato **JSON** ou **Form URL Encoded**). Se nenhum erro ocorrer, retorna um JSON com os dados do aluno. |
| DELETE | http://localhost:3000/alunos/:id | Deleta do banco de dados o aluno com o número de id especificado. Se nenhum erro ocorrer, retorna um JSON com os dados do aluno deletado. |
| PUT | http://localhost:3000/alunos/:id | Atualiza as informações de um aluno ao especificar o número de id e as informações que se deseja modificar (via corpo da requisição no formato **JSON** ou **Form URL Encoded**). Se a operação for concluída com êxito, retorna um JSON com os dados atualizados do aluno no formato. |