# Sistema de Solicitações de TI

Este projeto é uma implementação de um sistema de gerenciamento de solicitações de TI utilizando Google Apps Script. Ele permite que os usuários enviem solicitações por meio de um formulário do Google, e automaticamente envia um e-mail para o suporte de TI com os detalhes da solicitação.

## Funcionalidades

- **Recepção de solicitações**: O sistema recebe as respostas do formulário do Google.
- **Envio automático de e-mails**: As informações da solicitação são enviadas por e-mail para o suporte de TI.
- **Registro de logs**: Os erros e eventos são registrados no Logger para monitoramento.

## Pré-requisitos

- Acesso ao Google Workspace (Google Drive, Google Sheets, Google Forms).
- Conhecimento básico em Google Apps Script.

## Como Usar

1. **Criar um Formulário do Google**:
   - Crie um formulário que capture as seguintes informações:
     - Data e Hora
     - Título da Solicitação
     - Nome Completo (pode ter duas entradas)
     - Tipo de Solicitação
     - Localidade
     - AnyDesk (se aplicável)
     - Descrição do Problema
     - E-mail do Usuário

2. **Criar uma Planilha do Google**:
   - Conecte o formulário a uma planilha do Google onde as respostas serão registradas.

3. **Adicionar o Script**:
   - Abra a planilha do Google.
   - Vá para `Extensões > Apps Script`.
   - Cole o código do script fornecido neste repositório.

4. **Ativar o Gatilho**:
   - Execute a função `ativarGatilho` para configurar um gatilho que irá executar o envio do e-mail quando uma nova resposta for submetida.

5. **Testar**:
   - Preencha o formulário e envie uma solicitação. Verifique o e-mail do suporte de TI para confirmar o recebimento da solicitação.

## Estrutura do Código

O código é dividido em duas funções principais:

1. **`enviarEmailResposta(e)`**:
   - Recebe o evento do formulário.
   - Extrai os dados relevantes da resposta.
   - Compõe e envia um e-mail com as informações da solicitação.

2. **`ativarGatilho()`**:
   - Configura um gatilho para ativar a função `enviarEmailResposta` sempre que um novo formulário for enviado.

## Considerações Finais

Sinta-se à vontade para modificar e expandir o sistema conforme suas necessidades. Este projeto pode ser aprimorado com funcionalidades adicionais, como integração com um sistema de gerenciamento de tickets ou relatórios analíticos.

