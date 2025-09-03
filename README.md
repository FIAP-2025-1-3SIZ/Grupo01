1. Criar Usuário
Método: POST /usuarios

Códigos de Resposta:
201 Created: Sucesso. O usuário foi criado corretamente.
400 Bad Request: Erro. Os dados enviados eram inválidos (ex: e-mail sem @).
409 Conflict: Erro. O e-mail enviado já está cadastrado no sistema.

2. Listar todos os Usuários
Método: GET /usuarios

Códigos de Resposta:
200 OK: Sucesso. A lista de usuários foi retornada.
500 Internal Server Error: Erro. Ocorreu uma falha inesperada no servidor.

3. Buscar um Usuário por ID
Método: GET /usuarios/{id}

Códigos de Resposta:
200 OK: Sucesso. O usuário foi encontrado e seus dados foram retornados.
404 Not Found: Erro. Não existe um usuário com o ID informado.

4. Atualizar um Usuário (Completo)
Método: PUT /usuarios/{id}

Códigos de Resposta:
200 OK: Sucesso. O usuário foi atualizado com os novos dados.
400 Bad Request: Erro. Os dados enviados para a atualização eram inválidos.
404 Not Found: Erro. Não existe um usuário com o ID informado para ser atualizado.

5. Atualizar um Usuário (Parcial)
Método: PATCH /usuarios/{id}

Códigos de Resposta:
200 OK: Sucesso. O usuário foi atualizado com os campos informados.
400 Bad Request: Erro. O campo enviado para a atualização era inválido (ex: e-mail mal formatado).
404 Not Found: Erro. Não existe um usuário com o ID informado para ser atualizado.

6. Deletar um Usuário
Método: DELETE /usuarios/{id}

Códigos de Resposta:

204 No Content: Sucesso. O usuário foi deletado. (Nenhum corpo de dados é retornado).
404 Not Found: Erro. Não existe um usuário com o ID informado para ser deletado.
