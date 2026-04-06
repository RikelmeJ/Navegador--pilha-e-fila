Navegador--pilha-e-fila

Descrição do Problema e Visão Geral

Este projeto tem como objetivo simular o funcionamento dos botões voltar e avançar de um navegador web.

Em navegadores reais, ao acessar diferentes páginas, é possível retornar às páginas anteriores ou avançar novamente após ter voltado. Esse comportamento foi implementado utilizando a estrutura de dados **pilha (Stack)**, que segue o modelo LIFO (Last In, First Out).

O programa permite:

* Acessar novas páginas (URLs)
* Voltar para páginas anteriores
* Avançar para páginas futuras (quando possível)
* Visualizar o estado atual da navegação

Implementação

Foram utilizadas duas pilhas:

* **Pilha de Voltar (`Stack`)**: armazena o histórico de páginas visitadas
* **Pilha de Avançar (`Stack`)**: armazena páginas que podem ser acessadas novamente

Além disso, uma variável armazena a **página atual**.

Funcionamento do Sistema

Acessar nova página

* A página atual é adicionada à pilha de voltar
* A nova página se torna a página atual
* A pilha de avançar é limpa

Voltar

* A página atual vai para a pilha de avançar
* O topo da pilha de voltar se torna a nova página atual

Avançar

* A página atual vai para a pilha de voltar
* O topo da pilha de avançar se torna a nova página atual



Diagrama ilustrativo

Estado inicial após acessar páginas:

```text
Pilha Voltar: [Google, YouTube]
Página Atual: Instagram
Pilha Avançar: []
```

Após clicar em "Voltar":

```text
Pilha Voltar: [Google]
Página Atual: YouTube
Pilha Avançar: [Instagram]
```


 Principais Funções

* `acessar(String url)` → acessa uma nova página
* `voltar()` → retorna para a página anterior
* `avancar()` → avança para a próxima página
* `mostrarEstado()` → exibe o estado atual das pilhas


Entrada e  Saída

Entrada:

* URLs digitadas pelo usuário
* Escolhas no menu (acessar, voltar, avançar)

Saída:

* Página atual exibida
* Conteúdo das pilhas
* Mensagens informando ações realizadas
  


 Decisões de Implementação

* A pilha de avançar é sempre limpa ao acessar uma nova página, garantindo consistência no histórico.
* O sistema impede ações inválidas, como tentar voltar ou avançar quando não há páginas disponíveis.
* As pilhas são dinâmicas, permitindo crescimento automático conforme necessário.


Este projeto demonstra de forma prática a aplicação de pilhas em um cenário real, simulando o comportamento de navegação presente em navegadores modernos.


Juan Rikelme de Azevedo Aquino RA:972311029
Pedro Guilherme Alves Oliveira RA:972412169
