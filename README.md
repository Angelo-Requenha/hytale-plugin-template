# Hytale Plugin Template – Java (Gradle)

Este repositório foi criado com base no seguinte vídeo tutorial:

[https://www.youtube.com/watch?v=NEw9QjzZ9nM](https://www.youtube.com/watch?v=NEw9QjzZ9nM)

Ele serve como um template base para desenvolvimento de plugins/mods em Java para servidores Hytale, utilizando Gradle Wrapper para gerenciamento de build e dependências.

---

## Requisitos

* Java 21 instalado
* Git
* IntelliJ IDEA, VSCode ou outra IDE compatível com Java/Gradle

O servidor Hytale atualmente reconhece até **class file version 65 (Java 21)**.

---

## Usando este template para criar um novo plugin

Clone o repositório:

```bash
git clone git@github.com:Angelo-Requenha/hytale-plugin-template.git MeuNovoPlugin
cd MeuNovoPlugin
```

Ajuste conforme necessário:

* `group` e `name` no arquivo `build.gradle.kts`
* Pacote Java do projeto
* Classe principal do plugin

---

## Gerenciamento de dependências

O projeto utiliza **Gradle Wrapper**, portanto não é necessário instalar o Gradle manualmente.

No Windows:

```bash
gradlew build
```

No Linux/macOS:

```bash
./gradlew build
```

O Gradle Wrapper fará o download automático da versão correta do Gradle e das dependências do projeto.

---

## Gerando o arquivo `.jar`

Execute:

```bash
gradlew build
```

O arquivo `.jar` será gerado em:

```
build/libs/NomeDoPlugin-1.0-SNAPSHOT.jar
```

Copie este arquivo para a pasta `mods` do servidor Hytale.

---

## Execução no servidor

Após copiar o `.jar` para a pasta `mods`, inicie o servidor Hytale. O plugin será carregado durante a inicialização.

---

## Configuração do Java na IDE (exemplo IntelliJ)

Certifique-se de que o projeto está utilizando **Java 21**:

* `File → Project Structure → Project SDK → 21`
* `Settings → Build, Execution, Deployment → Build Tools → Gradle → Gradle JVM → 21`

---

## Estrutura básica do projeto

```
src/
 └─ main/
     ├─ java/
     └─ resources/
```

---

## Comandos úteis

| Comando                | Função                           |
| ---------------------- | -------------------------------- |
| `gradlew build`        | Compila o plugin                 |
| `gradlew clean`        | Limpa builds anteriores          |
| `gradlew dependencies` | Lista dependências do projeto    |
| `gradlew --version`    | Exibe a versão do Gradle Wrapper |

---

## Observações

* A pasta `build/` não deve ser versionada (já incluída no `.gitignore`)
* Em caso de erros relacionados à versão do Java, verifique se a compilação está configurada para Java 21
* Este template pode ser reutilizado como base para novos plugins, evitando a necessidade de reconfiguração inicial

---

## Créditos

A estrutura deste projeto foi baseada no vídeo tutorial indicado acima e adaptada para uso como template reutilizável.
