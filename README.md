# estudos-programacao

# 📚 Atividades da Faculdade

Repositório com as atividades e projetos que desenvolvo no curso de **Ciência da Computação** da **FURB** (Universidade de Blumenau).

## 👨‍💻 Sobre mim

Sou o **Matheus Raimundo da Silva**, estudante do 2º semestre de Ciência da Computação, em Blumenau (SC). Sou curioso, gosto de aprender novas tecnologias e estou construindo minha base para trabalhar com desenvolvimento de software.

[LinkedIn](https://linkedin.com/in/matheusraimundo-da-silva-a56712337)

---

## 📁 Projetos

| Projeto | Descrição | Tecnologias |
|---|---|---|
| [🎧 Sonora](sonora-fase05/) | Plataforma de streaming de áudio com músicas, podcasts, playlists, planos e anúncios | Java, JUnit, UML |

## 🎧 Destaque: Sonora

Plataforma de streaming de áudio feita em **Java**, para console, desenvolvida em fases. A pasta [`sonora-fase05`](sonora-fase05/) está na **Fase 05**, que trabalha **polimorfismo e interfaces**.

**O que o sistema faz**
- Cadastra músicas e podcasts em um acervo único
- Cadastra usuários com plano **Gratuito** (com anúncios) ou **Premium** (sem anúncios)
- Cria playlists com músicas e podcasts misturados
- Toca playlists, com um anúncio a cada 2 itens para o plano Gratuito
- Calcula a receita mensal da plataforma (planos + anúncios)

**Conceitos de POO aplicados**
- Herança e classes abstratas (`Conteudo`, `Plano`)
- Interfaces (`Cronometravel`, `Reproduzivel`, `Faturavel`)
- Polimorfismo, sem `if` de tipo
- Encapsulamento e validação de dados com exceções

**Qualidade**
- Testes unitários com **JUnit** (30 casos, baseados em planos de teste)
- Diagrama de classes **UML** com justificativa das associações

📖 Veja a documentação completa no [README do Sonora](sonora-fase05/README.md).

---

## 🛠️ Tecnologias e conceitos que estou estudando

- **Java** e lógica de programação
- **Programação orientada a objetos**
- **SQL** (DDL e DML)
- **Testes unitários** com JUnit
- **Modelagem** com diagramas de classes UML

---

## ▶️ Como rodar os projetos em Java

Pré-requisito: **JDK 17 ou superior**.

Dentro da pasta de cada projeto, compile e execute. Exemplo com o Sonora:

```bash
cd sonora-fase05
javac -d out src/*.java
java -cp out App
```

---

## 📬 Contato

- 📧 matheusraimundo2008@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/matheusraimundo-da-silva-a56712337)
