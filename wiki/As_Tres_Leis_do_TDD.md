# As Três Leis do TDD (Test Driven Development | "Desenvolvimento Orientado a Testes")

1. Você não é autorizado a escrever qualquer código de produção a não ser para fazer um teste unitário passar.
2. Você não é autorizado a escrever qualquer código adicional em um teste unitário do que o suficiente para fazer o teste falhar; e falhas de compilação são falhas.
3. Você não é autorizado a escrever qualquer código adicional de produção do que o suficiente para que o para fazer teste unitário falhando passar.

## Os três estágios do TDD: Vermelho-Verde-Refatorar

1. Escreva código de teste que falhe. (Vermelho)
2. Escreva código de produção para fazer o teste passar. (Verde)
3. Melhore o código do teste e o código de produção. (Refatorar)

*À medida que os testes ficam mais específicos, o código se torna mais genérico.*