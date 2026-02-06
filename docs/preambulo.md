<div class="alert alert-block alert-success" style="font-family:Times New Roman;color:#FFFFFF;background-color: #E7E7E7">
<h1 align="center"><span style="font-family:Times New Roman;color:#046D0B"><b>Ciencia de Datos para Investigación Aplicada usando Python</b></span></h1>
</div>
<br><br>

%## Contenido
%- [Preámbulo](#pre)
%- [Origenes: informática y programación](#s1)
%- [Top 10 lenguajes de programación](#s2)
%- [Ecosistema de Python](#s2)
%- [Aplicaciones con Python](#s4)

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
  <div class="languages-controls"><button onclick="languagesChangeSlide(-1)">Anterior</button><button onclick="languagesToggleAutoPlay()" id="languages-play-btn">Play</button><button onclick="languagesChangeSlide(1)">Siguiente</button><button onclick="languagesToggleFullscreen()" id="languages-fullscreen-btn">Pantalla completa</button></div>
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
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
}
.languages-controls button {
  margin: 0 5px;
  padding: 8px 15px;
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
.languages-slideshow-container.fullscreen {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  max-width: 100vw;
  z-index: 9999;
  background: #000;
  border: none;
  border-radius: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.languages-slideshow-container.fullscreen .languages-slides {
  max-height: calc(100vh - 80px);
  width: auto;
  max-width: 100%;
  object-fit: contain;
}
.languages-slideshow-container.fullscreen .languages-controls {
  position: absolute;
  bottom: 10px;
  width: 100%;
  background: rgba(0,0,0,0.5);
  padding: 15px;
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

  window.languagesToggleFullscreen = function() {
    const container = document.querySelector('.languages-slideshow-container');
    const fullscreenBtn = document.getElementById('languages-fullscreen-btn');
    
    if (!document.fullscreenElement) {
      container.requestFullscreen().then(() => {
        container.classList.add('fullscreen');
        fullscreenBtn.textContent = 'Salir';
      }).catch(err => {
        container.classList.add('fullscreen');
        fullscreenBtn.textContent = 'Salir';
      });
    } else {
      document.exitFullscreen().then(() => {
        container.classList.remove('fullscreen');
        fullscreenBtn.textContent = 'Pantalla completa';
      });
    }
  };

  document.addEventListener('fullscreenchange', function() {
    const container = document.querySelector('.languages-slideshow-container');
    const fullscreenBtn = document.getElementById('languages-fullscreen-btn');
    if (!document.fullscreenElement) {
      container.classList.remove('fullscreen');
      fullscreenBtn.textContent = 'Pantalla completa';
    }
  });

  languagesShowSlide(languagesSlideIndex);
})();
</script>


<br><br>
# Origenes: informatica y programación
<a name="s1"></a>
%---------------------------------------------------------------------------------------------------
Los origenes de la informática y la programación, y cómo evolucionaron para dar forma al mundo digital que conocemos hoy.

% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/lenguajes_pro.webp?raw=true
:name: fig:historiaLenguajes

:::
<br><br>
# Top 10 lenguajes de programación
<a name="s2"></a>
%---------------------------------------------------------------------------------------------------
Existen índices ([TIOBE](https://www.tiobe.com/tiobe-index/), [PYPL](https://pypl.github.io/ODE.html)) que miden la popularidad de los lenguajes de programación. Su principal utilidad es funcionar como 
un indicador de las tendencias actuales en el mundo de la programación, ayudando a desarrolladores y empresas
a tomar decisiones informadas sobre qué lenguajes aprender, enseñar o utilizar en nuevos proyectos.

:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/pypl.jpg?raw=true
:name: fig:pyplRanking

:::
<br><br>
# Ecosistema Python
<a name="s3"></a>
%---------------------------------------------------------------------------------------------------
El ecosistema Python es el conjunto de herramientas, bibliotecas, marcos de trabajo (frameworks) y la comunidad de desarrolladores que rodean al lenguaje de programación Python. Este ecosistema se caracteriza por su vastedad y la gran cantidad de recursos de código abierto, lo que permite a Python ser utilizado en una amplia variedad de campos, como el desarrollo web, la ciencia de datos, el aprendizaje automático y la informática científica. 

% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/ecosistema.png?raw=true
:name: fig:mountains
:align: center

:::
<br><br>
# Aplicaciones con Python
<a name="s4"></a>
%---------------------------------------------------------------------------------------------------
Python se utiliza para una gran variedad de aplicaciones debido a su versatilidad y a su extenso ecosistema. A continuación, se detallan algunas de las más importantes.
% A figure of a photograph of some mountains, followed by a caption
:::{figure} https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/preambulo/python_app.png?raw=true
:name: fig:pythonEcosistema
:align: center

:::



# Automatización de procesos
%<a name="s4"></a>
%---------------------------------------------------------------------------------------------------
%fabrica automatizada de tesla
<div class="responsive-video-container">
    <iframe src="https://www.youtube.com/embed/WYnOGAvQEgk?si=Ii5Hib0Wqff3t_15" title="YouTube video player - Fábrica automatizada de Tesla" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

% Data center automatizado
<div class="responsive-video-container">
    <iframe src="https://www.youtube.com/embed/YkctZlQgU0g?si=RgrtJYMFfJqO0s2K" title="YouTube video player - Data center automatizado" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

<style>
/* CSS para videos responsivos */
.responsive-video-container {
    position: relative;
    width: 100%;
    height: 0;
    padding-bottom: 56.25%; /* Aspect ratio 16:9 */
    margin: 20px 0;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.responsive-video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
}

/* Media queries para diferentes dispositivos */
/* Celulares pequeños */
@media screen and (max-width: 480px) {
    .responsive-video-container {
        margin: 15px 0;
        border-radius: 6px;
    }
}

/* Tablets */
@media screen and (min-width: 481px) and (max-width: 768px) {
    .responsive-video-container {
        max-width: 90%;
        margin: 20px auto;
    }
}

/* Laptops */
@media screen and (min-width: 769px) and (max-width: 1024px) {
    .responsive-video-container {
        max-width: 80%;
        margin: 25px auto;
    }
}

/* PCs y pantallas grandes */
@media screen and (min-width: 1025px) {
    .responsive-video-container {
        max-width: 70%;
        margin: 30px auto;
    }
}

/* Pantallas ultra grandes */
@media screen and (min-width: 1440px) {
    .responsive-video-container {
        max-width: 60%;
        margin: 35px auto;
    }
}
</style>
