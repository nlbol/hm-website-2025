+++
title = "Donaciones"
+++

[&#8592;]({{< ref "_index.md" >}})

Todas las horas están en GMT-4.


## **Donaciones**

💖 **Apoya el Hackmeeting Bolivia 0x7E9**

Si quieres apoyar el evento y ayudar a mantener la comunidad, puedes hacer una **donación**.  
¡Cada aporte cuenta para que más personas disfruten de charlas, talleres y actividades! 🙌


{{< raw >}}
<style>
/* Imagen pequeña */
.zoomable-img {
  cursor: pointer;
  width: 50%;
  max-width: 90%; /* responsive */
  border-radius: 6px;
  transition: transform 0.3s ease;
}

/* Contenedor fullscreen */
#zoom-modal {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease, background-color 0.3s ease;
  z-index: 9999;
  padding: 20px;
}

/* Modal activo */
#zoom-modal:target {
  opacity: 1;
  background-color: rgba(0,0,0,0.85);
  pointer-events: auto;
}

/* Imagen grande */
#zoom-modal img {
  max-width: 95%;
  max-height: 95%;
  width: auto;
  height: auto;
  border-radius: 10px;
  cursor: zoom-out;
  transform: scale(0.8);
  transition: transform 0.3s ease;
}

/* Imagen se agranda al mostrar modal */
#zoom-modal:target img {
  transform: scale(1);
}

/* Centrado de la imagen dentro del modal */
#zoom-modal a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}

/* ========================
   MEDIA QUERIES PARA MOVIL
   ======================== */
@media (max-width: 768px) {
  .zoomable-img {
    width: 70%; /* imagen más grande en móviles */
  }

  #zoom-modal {
    padding: 10px; /* menos padding en pantallas pequeñas */
  }

  #zoom-modal img {
    max-width: 100%;
    max-height: 90%;
  }
}
</style>

<!-- Imagen pequeña -->
<p style="text-align:center;">
  <a href="#zoom-modal">
    <img class="zoomable-img" src="/images/donaciones-hackmeeting-0x7e9.jpeg" alt="Donaciones">
  </a>
</p>

<!-- Modal fullscreen -->
<div id="zoom-modal">
  <!-- Imagen grande, clic para cerrar -->
  <a href="#">
    <img src="/images/donaciones-hackmeeting-0x7e9.jpeg" alt="Donaciones Grande">
  </a>
</div>
{{< /raw >}}



[&#8592;]({{< ref "_index.md" >}})
