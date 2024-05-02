# Criando-seu-Jogo-de-Mem-ria-Estilo-Genius

Para criar um jogo de memória estilo Genius, você vai precisar aplicar conceitos básicos de HTML, CSS e JavaScript. Vou te dar uma explicação geral e um exemplo prático dividido em módulos.

**Módulo 1: Estrutura HTML**
Comece criando a estrutura básica do seu jogo no HTML. Defina uma `div` principal que vai conter o jogo e `divs` menores para cada cor do jogo Genius.

```html
<div id="genius">
  <div id="verde" class="cor"></div>
  <div id="vermelho" class="cor"></div>
  <div id="amarelo" class="cor"></div>
  <div id="azul" class="cor"></div>
</div>
```

**Módulo 2: Estilização CSS**
Utilize CSS para estilizar o jogo. Com o CSS Grid, você pode facilmente organizar as cores em um layout quadriculado.

```css
#genius {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

.cor {
  width: 150px;
  height: 150px;
  cursor: pointer;
}

#verde { background-color: green; }
#vermelho { background-color: red; }
#amarelo { background-color: yellow; }
#azul { background-color: blue; }
```

**Módulo 3: Lógica JavaScript**
No JavaScript, você vai criar a lógica do jogo. Isso inclui a manipulação de arrays para definir a sequência de cores e arrow functions para lidar com eventos.

```javascript
const sequencia = [];
const cores = ['verde', 'vermelho', 'amarelo', 'azul'];

function adicionarCorNaSequencia() {
  const cor = cores[Math.floor(Math.random() * cores.length)];
  sequencia.push(cor);
}

function iniciarJogo() {
  adicionarCorNaSequencia();
}

document.querySelectorAll('.cor').forEach(cor => {
  cor.addEventListener('click', (evento) => {
    const corSelecionada = evento.target.id;
    // Verificar se a corSelecionada é a próxima cor da sequência
  });
});

iniciarJogo();
```

Esses são os módulos básicos para começar seu jogo Genius. A partir daqui, você pode adicionar mais funcionalidades, como verificar a sequência de cores, aumentar a dificuldade progressivamente e adicionar efeitos sonoros.
