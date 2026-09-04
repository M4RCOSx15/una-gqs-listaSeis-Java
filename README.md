# 🚀 Animação de Foguete no Terminal em Java

Este projeto consiste em um algoritmo simples, escrito em Java, que cria uma animação em estilo ASCII de um foguete decolando diretamente no seu terminal ou console.

## 📝 O que o algoritmo faz detalhadamente?

A ilusão de movimento e animação é alcançada através da rápida atualização do texto na tela do terminal. Aqui está o passo a passo de como o código funciona:

1. **Definição do Foguete (ASCII Art)**: O corpo estático do foguete é armazenado em um array de `String`, onde cada posição representa uma linha do desenho.
2. **Controle de Altitude (Loop `for`)**: A variável `alturaTerminal` define de onde o foguete vai começar. O laço `for` faz uma contagem regressiva. A cada iteração, ele imprime uma quantidade de linhas em branco (`\n`) igual ao valor atual da contagem. Conforme o número diminui, as linhas em branco diminuem, fazendo o foguete "subir".
3. **Limpeza de Tela (Clear Console)**: Para que a animação não crie um rastro no terminal, a tela é limpa a cada "quadro" (frame). Isso é feito usando o código de escape ANSI `\033[H\033[2J`, que move o cursor para o topo e apaga o conteúdo visível.
4. **Animação das Chamas**: Para dar vida ao foguete, o fogo saindo do propulsor não é estático. O algoritmo usa uma verificação matemática simples (`i % 2 == 0`, se o número da iteração é par ou ímpar) para alternar entre dois desenhos diferentes das chamas a cada quadro, criando um efeito de cintilação.
5. **Controle de Tempo (FPS)**: O comando `Thread.sleep(150)` obriga o programa a pausar por 150 milissegundos antes de desenhar o próximo quadro. Isso evita que a decolagem aconteça instantaneamente e dita a velocidade (taxa de quadros) da animação.

---

## 🛠️ Ferramentas e Tecnologias

Para criar e rodar este algoritmo, são utilizadas as seguintes ferramentas básicas:

*   **Java Development Kit (JDK)**: A ferramenta principal. É necessário para transformar o código em texto (`.java`) em código executável pela máquina virtual Java (comando `javac`) e para executar a aplicação (comando `java`).
*   **Editor de Texto ou IDE**: Onde o código foi escrito. Pode ser algo simples como o Bloco de Notas (Windows), Nano (Linux), ou ambientes robustos como VS Code, IntelliJ IDEA ou Eclipse.
*   **Terminal / Emulador de Terminal**: A interface de linha de comando onde a animação ocorre (Prompt de Comando, PowerShell, Terminal do Linux/macOS). *Nota: É necessário que o terminal suporte códigos de escape ANSI para que a limpeza de tela funcione corretamente.*

---

## 🚀 Como Executar

1. Certifique-se de ter o **Java (JDK)** instalado na sua máquina. Verifique abrindo o terminal e digitando: `java -version`.
2. Salve o código-fonte em um arquivo chamado `FogueteAnimacao.java`.
3. Abra o terminal e navegue até a pasta onde o arquivo foi salvo.
4. Compile o código com o comando:
   ```bash
   javac FogueteAnimacao.java
   ```
5. Após a compilação, execute o programa com o comando:
   ```bash
   java FogueteAnimacao
   ```
