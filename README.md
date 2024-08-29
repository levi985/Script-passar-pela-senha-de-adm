# Script RunAsInvoker

Este script permite contornar a solicitação de senha de administrador ao executar programas executáveis no Windows, utilizando a camada de compatibilidade `RUNASINVOKER`. É especialmente útil para usuários que frequentemente precisam executar aplicativos que normalmente exigem privilégios elevados.

## Como Funciona

O script funciona aproveitando a configuração de compatibilidade `RUNASINVOKER` no Windows. Quando você arrasta e solta um executável sobre o script, ele executa o programa com as permissões do usuário atual, em vez de solicitar credenciais de administrador.

## Conteúdo do Script

```batch
cmd /min /C "set __COMPAT_LAYER=RUNASINVOKER && start "" %1"
