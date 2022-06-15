# Aula 09 - Tratamento de Error

## Resumo do conteúdo da aula


### Tratando uma Excessão com `try`/`catch`/`finally`

```cs

try
{
    // Forçamos o erro ao tentar dividir um valor inteiro por 0.
    int calculo = 10 / 0;

    Console.WriteLine(calculo);
} 
catch(Exception error)
{
    // No bloco de tratamento do erro capturamos...
    Console.WriteLine("Código do Error AbCd123");
    // Tipo do Erro nesse techo do código.
    Console.WriteLine(error.GetType());
}
finally
{
    // Definimos uma instrução que deverá ser executada após o bloco try/catch.
    // Nota: Esse trecho de código será executado independente de existir uma excessão ou não.
    Console.WriteLine("Reinicie o programa...");
}

```

### Criando uma Excessão com `throw`

```cs

int capturaDaIdadeDoUsuario = Console.ReadLine();

bool valorCapturadoForValido = int.TryParse(capturaDaIdadeDoUsuario, out idadeDoUsuario);

if(valorCapturadoForValido) {
    Console.WriteLine(idadeDoUsuario);
}
else {
    // Uma Excessão é cadastrada para tratamento.
    throw new Exception("Valor inserido é inválido.");
}

```

## Materiais de apoio

- Atividades
    - [Mesa de trabalho](https://docs.google.com/document/d/1dtGLl0qcKBc-NdvUbwVNDUiCWPtVK8N0E1rbegRv7iE/edit?usp=sharing)
- Atividades resolvidas (Professor)
	- [Mesa de trabalho]()
- Atividade resolvida (Alunos)
	- [Mesa de trabalho](./ENTREGA.md)