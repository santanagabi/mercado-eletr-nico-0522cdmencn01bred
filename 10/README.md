# Aula 10 - Introdução a Orientação a Objeto

## Resumo do conteúdo da aula

### Encapsulamento

Agrupamos/Empasulamos em um contexto atributos e métodos em uma classe. 

```cs

class Lampada
{
    // Propriedade pública - Variáveis
    public string Fabricante = { get; set; };

    // Método Acessível/Público - Funções
    public virtual bool LigarOuDesligar()
    {

    }
}

```

### Abstração

Abstraimos/Privamos o acesso à atributos e métodos a partir de controladores de acesso. 

```cs

class Lampada
{
    public string Fabricante = { get; set; };
    
    // Definimos propriedades que serão Abstraídas/Privados de acesso.
    private int Voltagem = 110;

        
    // Definimos método que serão Abstraídos/Privados de acesso.
    private void GerarRelatorioDeUso() { }

    public virtual bool LigarOuDesligar()
    {

    }
}

```

### Herança

Herdamos os atributos e métodos implementados anteriormente, possibilitando o reaproveitando e implementação de novos recursos. 

```cs

class Lampada
{
    public string Fabricante = { get; set; };
    
    private int Voltagem = 110;

    private void GerarRelatorioDeUso() { }

    public virtual bool LigarOuDesligar()
    {

    }
}

// Herdamos os atributos e métodos da classe Lampada.
class Hue : Lampada {

    public void VariarIluminosidade()
    {

    }
}

```

### Polimorfismo

A partir de uma Herança, podemos sobrescrever recursos da classe herdada, sobrescrevendo alguns recursos herdados.

```cs

class Lampada
{
    public string Fabricante = { get; set; };

    private int Voltagem = 110;

    private void GerarRelatorioDeUso() { }

    public virtual bool LigarOuDesligar()
    {

    }
}

class Hue : Lampada
{

    public void VariarIluminosidade()
    {

    }

    // Sobrescrevemos a funcionalidade de ligar/Desligar.
    public override bool LigarOuDesligar() {

    }
}

```

## Materiais de apoio

- Atividades
    - [Mesa de trabalho](https://docs.google.com/document/d/1MIkJer795YBaOznAwBMRvsBUMDNxWJJKymU_R49CoYk/edit?usp=sharing)
- Atividades resolvidas (Professor)
	- [Mesa de trabalho]()
- Atividade resolvida (Alunos)
	- [Mesa de trabalho](./ENTREGA.md)