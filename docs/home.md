<div class="alert alert-block alert-success" style="font-family:Times New Roman;color:#FFFFFF;background-color: #E7E7E7">
<h1 align="center"><span style="font-family:Times New Roman;color:#046D0B"><b>Estadística para Investigación Usando Python</b></span></h1>
</div>
<br><br>

# Descripción del Curso

(Última actualización: 26 Agosto, 2025)

  Este curso está dividido en cuatro módulos interrelacionados. El primer módulo está diseñado para consolidar y profundizar en los fundamentos de programación, una habilidad indispensable para abordar los desafíos de la ciencia de datos de manera eficiente. Los módulos dos y tres se centran en el preprocesamiento y análisis avanzado de datos, proporcionando herramientas y técnicas esenciales para extraer valor de grandes volúmenes de información.
Finalmente, el cuarto módulo aborda los principios teóricos y prácticos del análisis de diseños experimentales, destacando su aplicación en la investigación científica y la toma de decisiones basada en evidencia.


# Objetivos
## General
Desarrollar aplicaciones para analizar y modelar datos utilizando el lenguaje de programación Python, con el fin de evaluar patrones, tendencias y realizar predicciones.

## Específicos
- Introducción a la computación en la nube (Google Colaboratory).
- Establecer bases en el conocimiento de programación básica emplenado el lenguaje de programación Python.
- Procesar, analizar y construir base de datos provenientes de archivos en formato CSV y XLSX.
- Emplear paquetes o librerias estándar de Python para generar gráficos descriptivos que permitan visualizar tendencias y patrones en datos procesados.
- Organizar y resumir datos para realizar pruebas de normalidad, hipótesis paramétricas y no paramétricas.
- Implementar modelos de regresión lineal simple. 

# Metodología
En este curso se utilizará una combinación de clases magistrales, debates en clase, presentaciones, videos, aprendizaje cooperativo y aprendizaje basado en problemas. Las calificaciones se determinarán según la entrega satisfactoria y puntual de las tareas. La calificación de cada tarea se basa en los prerrequisitos establecidos para cada una. A continuación, se presenta un resumen de los temas por cada sesión. Tenga en cuenta que las fechas y los plazos están sujetos a cambios.

# Plagio e Integridad Académica
El plagio es la práctica de copiar palabras, oraciones, imágenes o ideas para su uso en evaluaciones escritas u orales sin dar el crédito correspondiente a la fuente. Hacer trampa se define como dar o recibir ayuda ilegal en cualquier cosa que el profesor haya determinado como un esfuerzo individual. Ambas se consideran infracciones graves y afectarán significativamente la calificación del curso. 

:::{admonition} Evaluación
:class: warning %attention, caution, danger, error, important, hint, note, seealso, tip, warning
Se desarrollaran laboratorios por cada sesión, con los cuáles se determinará el promedio final (PF), Ecuación 1. La nota mínima
aprobatoria es 11.

:::{math}
:name: eq:pfinal
 PF = \sum_{i=1}^n  \frac{lab_{(i)} }{n}
:::
:::

# Herramientas
Para desarrollar este curso se recomienda usar la computación en la nube (Google Drive y Google Colaboratory). La siguiente secuancia de imágenes muestra cómo funciona la computación en la nube y como instalar
Google Colaboratory.

<div class="languages-slideshow-container">
  <img class="languages-slides active" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/cloudComputing/cc1.png?raw=true" alt="Imagen 0: Evolución 0">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/cloudComputing/cc2.png?raw=true" alt="Imagen 1: Evolución 1">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/cloudComputing/cc3.png?raw=true" alt="Imagen 2: Evolución 2">
  <img class="languages-slides" src="https://github.com/vrrp/sachabook_modulo1/blob/main/docs/images/cloudComputing/cc4.png?raw=true" alt="Imagen 3: Evolución 3">
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
