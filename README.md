# Gmail API Email List Script

Este repositório contém um script em Python que autentica e lista e-mails de uma conta do Gmail usando a API do Gmail. O script permite a listagem de e-mails com base em uma consulta especificada.

## Requisitos

- Python 3.6 ou superior
- Bibliotecas Python:
  - `google-auth`
  - `google-auth-oauthlib`
  - `google-auth-httplib2`
  - `google-api-python-client`
- Credenciais de API do Google configuradas para o projeto

## Configuração

### 1. Ativar a API do Gmail

- Acesse o [Google Cloud Console](https://console.cloud.google.com/).
- Crie um novo projeto ou selecione um existente.
- Ative a API do Gmail.
- Acesse as "Credenciais" e crie um "ID do cliente OAuth 2.0".
- Baixe o arquivo `credentials.json`.

### 2. Instalar Dependências

Instale as bibliotecas necessárias usando pip:

```bash
pip install google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client
```

### 3. Colocar o Arquivo de Credenciais

Coloque o arquivo `credentials.json` no diretório raiz do projeto.

## Execução

1. Execute o script Python:

   ```bash
   python gmail_list_emails.py
   ```

2. Na primeira execução, o navegador abrirá solicitando permissões para acessar o Gmail. Conceda as permissões e o token de autenticação será salvo como `token.json`.
3. O script listará os e-mails com base na consulta especificada.

## Personalização

### Modificar a Consulta de Listagem

A consulta pode ser modificada no código:

```python
query = 'is:unread'
```

Substitua `is:unread` pela consulta desejada. Por exemplo, `from:example@example.com` para listar e-mails de um remetente específico.

## Funções do Script

### `authenticate_gmail()`

Autentica o usuário no Gmail e retorna as credenciais.

### `list_emails(service, query)`

Lista e-mails com base na consulta fornecida. Imprime o assunto, remetente, data e corpo de cada e-mail encontrado.

## Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

