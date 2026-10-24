# 🎧 Sonora

Plataforma de streaming de áudio feita em **Java**, para console. Projeto acadêmico do curso de Ciência da Computação (FURB), desenvolvido em fases, com foco em **programação orientada a objetos**.

Este repositório contém a **Fase 05**, que trabalha **polimorfismo e interfaces**.

---

## ✨ O que o Sonora faz

- Cadastra **músicas** e **podcasts** em um acervo único
- Cadastra **usuários** com plano **Gratuito** (com anúncios) ou **Premium** (sem anúncios)
- Cria **playlists** com músicas e podcasts misturados
- Permite **seguir** e deixar de seguir outros usuários
- **Toca playlists**: ouvintes do plano Gratuito recebem um anúncio a cada 2 itens
- Calcula a **receita mensal** da plataforma (mensalidades dos planos + anúncios por impressões)
- Lista os episódios de um apresentador

---

## 🧠 Conceitos de POO aplicados

| Conceito | Onde aparece |
|---|---|
| **Herança** | `Musica` e `Podcast` herdam de `Conteudo`; `PlanoGratuito` e `PlanoPremium` herdam de `Plano` |
| **Classes abstratas** | `Conteudo` (com `getCreditos()` abstrato) e `Plano` (com `temAnuncios()` abstrato) |
| **Interfaces** | `Cronometravel`, `Reproduzivel` (que estende `Cronometravel`) e `Faturavel` |
| **Polimorfismo** | `Playlist` e `Plataforma` guardam `ArrayList<Conteudo>` e tratam músicas e podcasts do mesmo jeito, sem `if` de tipo |
| **Método `default`** | `Cronometravel.getDuracaoFormatada()` |
| **Encapsulamento** | Atributos privados, construtores que validam os dados e lançam `IllegalArgumentException` |
| **Tipo estático x dinâmico** | Comentado no `main` do `App`; `instanceof` com cast usado apenas em `listarEpisodiosDe` |

### Destaque: `Anuncio` sem herança

`Anuncio` não herda de `Conteudo` nem de `Plano`. Ele implementa duas interfaces: **`Reproduzivel`** (toca como um conteúdo) e **`Faturavel`** (gera receita como um plano). Por isso `calcularReceitaMensal()` soma planos e anúncios em **um único laço** sobre `ArrayList<Faturavel>`.

---

## 📐 Diagrama de classes

![Diagrama de classes do Sonora](docs/diagrama-classes.png)

A justificativa das associações (nome, papéis, multiplicidade e navegabilidade) está em [`docs/modelagem.md`](docs/modelagem.md).

---

## 🗂️ Estrutura do projeto

```
sonora-fase05/
├── docs/
│   ├── diagrama-classes.png
│   ├── diagrama-classes.svg
│   └── modelagem.md
├── src/        App, Plataforma, Playlist, Usuario, Conteudo, Musica, Podcast,
│               Plano, PlanoGratuito, PlanoPremium, Anuncio,
│               Cronometravel, Reproduzivel, Faturavel
├── test/       Testes JUnit
├── planos-de-teste.md
└── README.md
```

---

## ▶️ Como rodar

Pré-requisito: **JDK 17 ou superior**.

```bash
javac -d out src/*.java
java -cp out App
```

### Roteiro rápido de demonstração

1. Opção **2**: cadastre um usuário no plano **Gratuito** e outro no **Premium**
2. Opção **13**: cadastre um ou dois anúncios
3. Opção **3**: crie uma playlist com músicas e podcasts do acervo inicial
4. Opção **17**: veja a receita mensal (só a mensalidade do Premium)
5. Opção **15**: toque a playlist para o usuário Gratuito e veja os anúncios aparecerem
6. Opção **17** de novo: a receita aumenta com as impressões dos anúncios

---

## 🧪 Testes

Os testes foram escritos com **JUnit** a partir de [planos de teste](planos-de-teste.md) (30 casos). Eles cobrem:

- formatação da duração (`getDuracaoFormatada`)
- validação dos construtores com dados inválidos
- sequência de ids sem "buracos" após tentativas inválidas
- comportamento de `Playlist` e `Plataforma`

Para rodar (precisa do `junit-platform-console-standalone` salvo como `junit-console.jar`):

```bash
javac -d out -cp junit-console.jar src/*.java test/*.java
java -jar junit-console.jar execute --class-path out --scan-class-path
```

---

## 🛠️ Tecnologias

- Java
- JUnit
- UML (diagrama de classes)

---

## 👨‍💻 Autor

**Matheus Raimundo da Silva**
Estudante de Ciência da Computação na FURB — Blumenau, SC

[LinkedIn](https://linkedin.com/in/matheusraimundo-da-silva-a56712337)
