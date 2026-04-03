**Especificação de Casos de Uso - Sistema de Trocas**

*Realizar Login (Usuário)*
Ator: Usuário

Descrição: Permite que o usuário acesse o sistema utilizando suas credenciais.

Pré-condições:
O usuário deve estar previamente cadastrado.

Fluxo Principal:
O usuário acessa a tela de login.
Informa suas credenciais (e-mail e senha).
O sistema valida os dados.
O sistema concede acesso ao usuário.

Fluxos Alternativos:
Credenciais inválidas:
O sistema exibe mensagem de erro.
O usuário pode tentar novamente.

Pós-condições:
Usuário autenticado no sistema.

======================================================================
*Acessar Perfil*
Ator: Usuário

Descrição: Permite visualizar e editar informações pessoais.

Pré-condições:
Usuário autenticado.

Fluxo Principal:
O usuário acessa seu perfil.
O sistema exibe os dados cadastrados.

Extensões:
Alterar dados pessoais.

======================================================================
*Acessar Notas de Troca*
Ator: Usuário

Descrição: Permite visualizar suas notas de troca.
Pré-condições:
Usuário autenticado.

Fluxo Principal:
O usuário acessa a área de notas.
O sistema lista as notas disponíveis.
O usuário seleciona uma nota.
O sistema exibe os detalhes e o código de barras.

Relacionamentos:
<> Ler código de barras
<> Realizar troca

======================================================================
*Realizar Troca*
Atores: Usuário, Funcionário

Descrição: Permite realizar a troca de um produto.

Pré-condições:
Nota de troca válida.
Código de barras disponível.

Fluxo Principal:
O funcionário solicita o código de barras.
O sistema realiza a leitura.
O sistema valida a nota.
O funcionário efetua a troca.
O sistema registra a operação.

Fluxos Alternativos:
Código inválido:
O sistema informa erro.
A troca não é realizada.

Pós-condições:
Troca registrada no sistema.

======================================================================
*Ler Código de Barras*
Ator: Funcionário

Descrição: Permite a leitura de códigos de barras para validação.

Pré-condições:
Sistema operacional ativo.

Fluxo Principal:
O funcionário inicia a leitura.
O sistema captura o código.
O sistema processa e valida o código.

Pós-condições:
Código identificado no sistema.

======================================================================
*Registrar Usuário*
Ator: Funcionário

Descrição: Permite cadastrar novos usuários.

Fluxo Principal:
O funcionário acessa o cadastro.
Insere os dados do usuário.
O sistema valida as informações.
O sistema salva o cadastro.

======================================================================
*Alterar Usuário*
Ator: Funcionário

Descrição: Permite atualizar dados de um usuário.

Fluxo Principal:
O funcionário busca o usuário.
Altera os dados necessários.
O sistema salva as alterações.

======================================================================
*Registrar Troca*
Ator: Funcionário

Descrição: Registra uma nova nota de troca.

Fluxo Principal:
O funcionário acessa o módulo de trocas.
Insere os dados da troca.
O sistema gera a nota com código de barras.

======================================================================
*Registrar Funcionário*
Ator: Gerente

Descrição: Permite cadastrar novos funcionários.

Fluxo Principal:
O gerente acessa o módulo de funcionários.
Insere os dados.
O sistema valida e salva o cadastro.

======================================================================
*login (Funcionário e Gerente)*
Atores: Funcionário, Gerente

Descrição: Permite acesso administrativo ao sistema.

Fluxo Principal:
O ator acessa a tela de login.
Informa credenciais.
O sistema valida.
O sistema concede acesso conforme nível de permissão.

Pós-condições:
Acesso autorizado com permissões específicas.


