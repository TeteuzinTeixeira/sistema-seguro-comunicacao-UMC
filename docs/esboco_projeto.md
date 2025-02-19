# Objetivo do Projeto

O objetivo deste projeto é garantir a **segurança na comunicação** entre os funcionários da empresa.

## Tecnologias Utilizadas

- **bcrypt**: Hashing seguro de senhas.
- **PyJWT**: Autenticação via Tokens JWT.
- **cryptography**: Implementação de algoritmos de criptografia como AES e RSA.

## Fluxo Básico

1. **Cadastro do Usuário**:  
   O usuário realiza o cadastro e sua senha é armazenada de forma segura utilizando **bcrypt**.

2. **Login do Usuário**:  
   O usuário faz login e é autenticado através de **Tokens JWT**.

3. **Envio de Mensagem**:  
   O usuário envia uma mensagem criptografada utilizando o algoritmo **AES**.

4. **Descriptografia da Mensagem**:  
   Somente o destinatário correto poderá descriptografar a mensagem com sua chave **RSA**.

## Benefícios

- **Segurança** aprimorada no armazenamento e comunicação de dados sensíveis.
- **Proteção de senhas** utilizando hashing.
- **Autenticação eficiente** com Tokens JWT.
- **Criptografia de ponta a ponta** para a troca de mensagens.
