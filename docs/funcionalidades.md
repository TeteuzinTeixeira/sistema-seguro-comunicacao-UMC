## Descrição clara do que o sistema faz, de forma simples:

- **Cadastro de usuário** → Protege a senha com bcrypt antes de armazenar.
- **Login** → Se a senha estiver correta, gera um Token JWT.
- **Enviar mensagem** → A mensagem é criptografada com AES antes de ser salva.
- **Receber mensagem** → O usuário descriptografa com RSA sua chave AES e acessa a mensagem.

## Cadastro de Usuário

### Hash de senha com bcrypt:

- O bcrypt é usado para gerar um hash seguro a partir da senha do usuário.
- Este hash é armazenado no banco de dados em vez da senha em texto plano.
- Bcrypt utiliza um algoritmo de hashing adaptativo, o que significa que é resistente a ataques de força bruta.

## Login

### Geração e verificação de Token JWT:

- Ao fazer login, um token JWT (JSON Web Token) é gerado e enviado para o usuário.
- Este token contém informações de autenticação e é assinado para garantir sua integridade.
- Durante ações subsequentes, o token é verificado para validar a identidade do usuário.

## Criptografia de Mensagens

### Uso de AES (CBC):

- AES (Advanced Encryption Standard) é usado para criptografar as mensagens dos usuários.
- O modo de operação CBC (Cipher Block Chaining) oferece segurança adicional ao criptografar cada bloco de dados com a combinação do bloco anterior.

## Proteção da Chave AES

### Uso de RSA para criptografar a chave antes de armazená-la:

- RSA é um algoritmo de criptografia assimétrica utilizado para proteger a chave AES.
- A chave AES é criptografada com a chave pública RSA antes de ser armazenada.
- Apenas a chave privada RSA pode descriptografar a chave AES, garantindo segurança.

## Armazenamento Seguro de Dados

- Os dados criptografados são armazenados em um banco de dados seguro.
- Medidas adicionais de segurança, como acesso restrito e monitoramento de atividades, são implementadas para proteger os dados contra acessos não autorizados.
- Backups regulares e criptografados são mantidos para garantir a recuperação de dados em caso de falhas.
