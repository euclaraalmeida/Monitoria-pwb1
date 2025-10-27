# Conceitos inicias - CSS

### .class
Vários elementos podem usar o mesmo uniforme para terem o mesmo
visual. Você usa classes para qualquer estilo que queira reutilizar,
como .botao, .card, ou .texto-destaque.

### #id 
Ele só pode ser usado por um único elemento na página. Exemplo no
seu menu, você coloca um link como "Sobre". Esse href com hashtag diz ao
navegador: "Procure o elemento com esse Id. \<section id="Sobre-nos" Lá
embaixo na sua página vai ser direcionado para essa parte da pagina você
dá esse RG para a sua seção:
```{=html}
<section id="Sobre-nos">
```

### CSS Inline 
(No Atributo style) Você escreve o CSS diretamente dentro da tag HTML usando o atributo style. É rápido para testes, mas não é recomendado porque mistura estilo com conteúdo e não pode ser reutilizado.

```{=html}
 Exemplo: <p style="color: red;">Este texto fica vermelho.</p>
```
### CSS Interno 
(Na Tag <style>) Você coloca seu código CSS dentro de uma tag <style> no <head> do seu arquivo HTML. Os estilos afetam apenas essa página , mas é mais organizado que o inline.
```{=html}
Exemplo: No <head>, você teria <style> p { color: blue; } </style>.
```

### CSS Externo 
(Arquivo .css Linkado) Esta é a melhor prática. Você escreve todo o seu CSS em um arquivo separado (ex: style.css) e o "linka" no <head> do seu HTML. Isso mantém seu HTML limpo e permite que vários arquivos HTML usem o mesmo CSS, facilitando a manutenção.
```{=html}
Exemplo: No <head>, você teria <link rel="stylesheet" href="style.css">.
```
### Responsividade 
É a técnica de fazer seu site se adaptar e funcionar bem
em qualquer tamanho de tela, seja um celular, tablet ou desktop. Em vez
de ter um layout fixo, ele "responde" e muda de aparência.

A forma mais comum de fazer isso é com a abordagem Mobile First. Nela,
você primeiro cria o CSS base para o celular (que é mais simples) e,
depois, usa Media Queries (regras @media) para aplicar estilos
diferentes em telas maiores.

```{=html}
Mobile first - base

 . container {
 display : flex ; flex - direction :
column ;
}

. sidebar { width : 100%; }
```

A @media (ou Media Query) é a ferramenta principal da responsividade.
Ela permite que você aplique estilos CSS diferentes apenas quando uma
condição específica é atendida, como o tamanho da tela.
```{=html}
@media (min-width: 768px) { ... }
```

