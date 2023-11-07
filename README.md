# repositorio_caixa_eletronico

//
INICIO principal

VAR valor: INTEIRO

VAR Salor: INTEIRO

VAR encerrar_programa: BOOLEANO

DEFINIR encerrar_programa -> falso

ENQUANTO encerrar_programa IGUAL_A falso
CHAMAR MOSTRAR_MENU -> opcao_selecionada
SE opcao_selecionada IGUAL_A a
MOSTRAR "Seu Saldo é : ", Saldo
OU_SE opcao_selecionada IGUAL_A b
MOSTRAR " Digite o valor a despositar: "
ESPERAR_DIGITACAO -> valor
SOMAR valor, saldo -> saldo
MOSTRAR "Deposito efetuado"
OU_SE opcao_selecionada IGUAL_A c
MOSTRAR "Digite o valor a retirar: "
ESPERAR_DIGITACAO -> valor
SE valor MAIOR_QUE saldo
MOSTRAR " Saque não permitido, saldo insuficiente"
SENAO
SUBTRAIR valor, saldo -> saldo
FIM SE
MOSTRAR "Saque efetuado"
OU_SE opcao_selecionada IGUAL_A d
DEFINIR verdadeiro -> encerrar_programa
SENAO
MOSTRAR "opcao inválida, tente novamente"
FIM ENQUANTO
FINAL

INICIO MOSTRAR_MENU
VAR opcao_selecionada: STRING
MOSTRAR "Menu de operacao"
MOSTRAR "[a] Mostrar Saldo"
MOSTRAR "[b] Mostrar Deposito"
MOSTRAR "[c] Mostrar Saque"
MOSTRAR "[d] Mostrar Finalizar"
ESPERAR_DIGITACAO -> opcao_selecionada
RETORNAR opcao_selecionada
FIM MOSTRAR_MENU
