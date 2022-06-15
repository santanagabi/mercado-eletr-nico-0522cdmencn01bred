# Aula 11 - Controladores de acesso

## Resumo do conteúdo da aula

### Sintaxe


#### Modificador de classe / Controlador de acesso

**Modificador Classe:** Define a visibilidade/comportamento da Classe.

**Controlador de Acesso:** Especifica em que momento* um membro da Classe poderá ser acessível.

**Nota:** Membros = atributos e métodos.

```cs

[Modificador Classe] class Lampada
{

    [Controlador de Acesso] string Fabricante = { get; set; };

    [Controlador de Acesso] virtual bool LigarOuDesligar()
    {

    }
}

```

### Lista de modificadores de visibilidade/comportamento da classe

**public**: Sem restrições de visibilidade.

**abstract**: Classe-base para outras classes, não podem ser instânciadas.

**sealed**: Classe não permite herança.

**static**: Classe pode ser utilizanda sem a necessidade de instânciá-la.


### Lista de controladores de acesso dos membros da classe

**public**: Sem restrição de acesso.

**private**: Só podem ser acessados pela própria classe.

**protected**: Podem ser acessados pela própria classe e por classes derivadas/herdeiras.

**virtual**: Permite que o método possa ser redefinido por classes derivadas/herdeiras.

**static**: Permite que os membros da classe possam ser acessados sem a necessidade de instânciar a classe.


## Materiais de apoio

- Atividades
    - [Mesa de trabalho]()
- Atividades resolvidas (Professor)
	- [Mesa de trabalho]()
- Atividade resolvida (Alunos)
	- [Mesa de trabalho](./ENTREGA.md)