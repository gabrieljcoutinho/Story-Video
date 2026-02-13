# Story
Este projeto é uma aplicação web minimalista que exibe vídeos em tela cheia, permitindo a navegação entre eles através do scroll do mouse ou de forma automática. É ideal para apresentações de portfólios ou visualização de conteúdos curtos em estilo de "feed".

---

## Estrutura do Projeto

O código está organizado em uma estrutura única de HTML5 que engloba o estilo (CSS) e a lógica de controle (JavaScript).

### Componentes Principais

* **HTML5:** Define a estrutura do contêiner e a lista de fontes de vídeo.
* **CSS3:** Garante que a interface seja focada no conteúdo, utilizando fundo escuro e centralização absoluta.
* **JavaScript:** Gerencia a troca de vídeos, detecção de eventos de scroll e a reprodução aleatória inicial.

---

## Funcionalidades Detalhadas

### 1. Navegação por Scroll
O código monitora o evento de roda do mouse (`wheel`). 
* **Scroll para baixo:** Avança para o próximo vídeo.
* **Scroll para cima:** Retorna ao vídeo anterior.

### 2. Reprodução Contínua
Cada vídeo possui um ouvinte de evento `ended`. Assim que o vídeo atual chega ao fim, a função `scrollToNextVideo()` é disparada automaticamente, criando um loop infinito de conteúdo.

### 3. Sistema de Exibição
Para evitar sobrecarga de áudio e processamento, o script garante que apenas um vídeo tenha a propriedade `display: block` e o comando `.play()` ativos por vez. Todos os outros são pausados e ocultados.

---

## Como Configurar

1.  **Arquivos de Vídeo:**
    Certifique-se de que os vídeos estão na pasta correta. O código espera a seguinte estrutura:
    ```text
    /seu-projeto
    ├── index.html
    └── Videos/
        ├── Lamborghini.mp4
        ├── McLarenDançaKonduro.mp4
        └── (demais arquivos...)
    ```

2.  **Edição da Lista:**
    Para adicionar novos vídeos, basta inserir uma nova tag `<video>` ao final do arquivo HTML seguindo o modelo:
    ```html
    <video controls>
        <source src="./Videos/nome_do_seu_video.mp4" type="video/mp4">
    </video>
    ```

---

## Tecnologias Utilizadas

* **Layout:** Flexbox para centralização.
* **Estilização:** CSS interno (Internal Stylesheet).
* **Lógica:** JavaScript nativo (Vanilla JS).

---

## Notas de Compatibilidade
Alguns navegadores (como Chrome e Safari) possuem políticas rígidas de **Autoplay**. Se os vídeos não iniciarem automaticamente com som, pode ser necessário adicionar o atributo `muted` nas tags de vídeo ou garantir uma interação prévia do usuário com a página.
https://github.com/user-attachments/assets/fa7a3d92-e3a1-48a5-b2ff-90d3b96e1c14
