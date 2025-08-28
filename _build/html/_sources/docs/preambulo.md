<div class="alert alert-block alert-success" style="font-family:Times New Roman;color:#FFFFFF;background-color: #E7E7E7">
<h1 align="center"><span style="font-family:Times New Roman;color:#046D0B"><b>Procesamiento de Datos con Inteligencia Artificial</b></span></h1>
</div>
<br><br>

## Contenido
- [Preámbulo](#pre)
- [Origenes: informática y programación](#s1)
- [Top 10 lenguajes de programación](#s2)
- [Ecosistema de Python](#s2)
- [Aplicaciones con Python](#s4)

# Preámbulo
<a name="pre"></a>
%---------------------------------------------------------------------------------------------------
La sociedad ha experimentado una evolución significativa a lo largo del tiempo, marcada por avances tecnológicos y cambios en las necesidades y capacidades humanas.

<div class="languages-slideshow-container">
  <img class="languages-slides active" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/rev0.png?raw=true" alt="Imagen 0: Evolución 0">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/rev1.png?raw=true" alt="Imagen 1: Evolución 1">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/rev2.png?raw=true" alt="Imagen 2: Evolución 2">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/rev3.png?raw=true" alt="Imagen 3: Evolución 3">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/rev4.png?raw=true" alt="Imagen 4: Evolución 4">
  <div class="languages-controls">
    <button onclick="languagesChangeSlide(-1)">Anterior</button>
    <button onclick="languagesToggleAutoPlay()" id="languages-play-btn">Play</button>
    <button onclick="languagesChangeSlide(1)">Siguiente</button>
  </div>
</div>

<style>
.languages-slideshow-container {
  max-width: 800px;
  margin: auto;
  position: relative;
  border: 2px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}
.languages-slides {
  display: none;
  width: 100%;
  height: auto;
}
.languages-slides.active {
  display: block;
}
.languages-controls {
  text-align: center;
  margin-top: 10px;
  padding: 10px;
}
.languages-controls button {
  margin: 0 10px;
  padding: 10px 20px;
  cursor: pointer;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 14px;
  transition: background-color 0.3s;
}
.languages-controls button:hover {
  background: #0056b3;
  transform: translateY(-2px);
}
</style>

<script>
(function() {
  let languagesSlideIndex = 0;
  let languagesAutoPlayInterval = null;
  const languagesSlides = document.getElementsByClassName("languages-slides");
  const languagesPlayBtn = document.getElementById("languages-play-btn");

  function languagesShowSlide(index) {
    if (index >= languagesSlides.length) languagesSlideIndex = 0;
    if (index < 0) languagesSlideIndex = languagesSlides.length - 1;
    for (let i = 0; i < languagesSlides.length; i++) {
      languagesSlides[i].classList.remove("active");
    }
    languagesSlides[languagesSlideIndex].classList.add("active");
  }

  window.languagesChangeSlide = function(n) {
    languagesSlideIndex += n;
    languagesShowSlide(languagesSlideIndex);
  };

  window.languagesToggleAutoPlay = function() {
    if (languagesAutoPlayInterval) {
      clearInterval(languagesAutoPlayInterval);
      languagesAutoPlayInterval = null;
      languagesPlayBtn.textContent = "Play";
    } else {
      languagesAutoPlayInterval = setInterval(() => {
        languagesSlideIndex++;
        languagesShowSlide(languagesSlideIndex);
      }, 3000); // Cambia cada 3 segundos
      languagesPlayBtn.textContent = "Pause";
    }
  };

  languagesShowSlide(languagesSlideIndex);
})();
</script>



# Origenes: informatica y programación
<a name="s1"></a>
%---------------------------------------------------------------------------------------------------
Los origenes de la informática y la programación, y cómo evolucionaron para dar forma al mundo digital que conocemos hoy.

% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/lenguajes_pro.webp?raw=true
:name: fig:historiaLenguajes

xx
:::

# Top 10 lenguajes de programación
<a name="s2"></a>
%---------------------------------------------------------------------------------------------------
Existen índices ([TIOBE](https://www.tiobe.com/tiobe-index/), [PYPL](https://pypl.github.io/ODE.html)) que miden la popularidad de los lenguajes de programación. Su princiupal utilidad es funcionar como 
un indicador de las tendencias actuales en el mundo de la programación, ayudando a desarrolladores y empresas
a tomar decisiones informadas sobre qué lenguajes aprender, enseñar o utilizar en nuevos proyectos.

:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/pypl.jpg?raw=true
:name: fig:historiaLenguajes

:::

# Ecosistema Python
<a name="s3"></a>
%---------------------------------------------------------------------------------------------------
El ecosistema Python es el conjunto de herramientas, bibliotecas, marcos de trabajo (frameworks) y la comunidad de desarrolladores que rodean al lenguaje de programación Python. Este ecosistema se caracteriza por su vastedad y la gran cantidad de recursos de código abierto, lo que permite a Python ser utilizado en una amplia variedad de campos, como el desarrollo web, la ciencia de datos, el aprendizaje automático y la informática científica. 

% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/ecosistema.png?raw=true
:name: fig:mountains
:align: center

:::

# Aplicaciones con Python
<a name="s4"></a>
%---------------------------------------------------------------------------------------------------
Python se utiliza para una gran variedad de aplicaciones debido a su versatilidad y a su extenso ecosistema. A continuación, se detallan algunas de las más importantes.
% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/python_app.png?raw=true
:name: fig:mountains
:align: center

:::


<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="https://www.youtube.com/embed/EaETjKmXOTo?si=uAeOYk-SXi9tKXkV" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" allowfullscreen></iframe>
</div>
