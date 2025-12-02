+++
title = "Difusión"
+++

[&#8592;]({{< ref "_index.md" >}})

## Difusiones voluntarias  
{{< raw >}}
<div class="video-player-container">
  <div class="video-wrapper">
    <video 
      id="main-video"
      class="responsive-video"
      controls
      controlsList="nodownload"
      preload="metadata"
      playsinline
      webkit-playsinline
      poster=""
      onloadedmetadata="adjustVideoAspect()"
    >
      <source src="videos/0x7e9.mp4" type="video/mp4">
      <p>Tu navegador no soporta el elemento de video. 
         <a href="videos/0x7e9.mp4">Descarga el video aquí</a>.
      </p>
    </video>
    
    <!-- Overlay de controles personalizados -->
    <div class="custom-controls-overlay">
      <button class="fullscreen-toggle" onclick="toggleFullScreen()" aria-label="Pantalla completa">
        <svg class="fullscreen-enter" width="24" height="24" viewBox="0 0 24 24" fill="white">
          <path d="M7 14H5v5h5v-2H7v-3zm-2-4h2V7h3V5H5v5zm12 7h-3v2h5v-5h-2v3zM14 5v2h3v3h2V5h-5z"/>
        </svg>
        <svg class="fullscreen-exit" width="24" height="24" viewBox="0 0 24 24" fill="white">
          <path d="M5 16h3v3h2v-5H5v2zm3-8H5v2h5V5H8v3zm6 11h2v-3h3v-2h-5v5zm2-11V5h-2v5h5V8h-3z"/>
        </svg>
      </button>
    </div>
    
    <!-- Indicador de carga -->
    <div class="video-loading" id="loading-indicator">
      <div class="spinner"></div>
      <span>Cargando video...</span>
    </div>
  </div>
</div>

<style>
/* Contenedor principal */
.video-player-container {
  width: 100%;
  margin: 0 auto;
  padding: 0;
  position: relative;
  background: #000;
}

/* Wrapper que mantiene la relación de aspecto */
.video-wrapper {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%; /* Relación 16:9 por defecto */
  overflow: hidden;
  background: #000;
}

/* Video que se ajusta al contenedor */
.responsive-video {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 100%;
  transform: translate(-50%, -50%);
  object-fit: contain; /* Mantiene toda la imagen visible sin recortar */
  background: #000;
}

/* Controles personalizados */
.custom-controls-overlay {
  position: absolute;
  bottom: 20px;
  right: 20px;
  z-index: 100;
  opacity: 0.8;
  transition: opacity 0.3s ease;
}

.video-wrapper:hover .custom-controls-overlay {
  opacity: 1;
}

.fullscreen-toggle {
  background: rgba(0, 0, 0, 0.7);
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  width: 50px;
  height: 50px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  backdrop-filter: blur(5px);
}

.fullscreen-toggle:hover {
  background: rgba(0, 0, 0, 0.9);
  border-color: rgba(255, 255, 255, 0.7);
  transform: scale(1.1);
}

.fullscreen-exit {
  display: none;
}

/* Indicador de carga */
.video-loading {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
  z-index: 50;
  display: none;
}

.spinner {
  width: 40px;
  height: 40px;
  border: 4px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  border-top-color: white;
  animation: spin 1s ease-in-out infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* Estados de pantalla completa */
.video-player-container:-webkit-full-screen .video-wrapper {
  width: 100vw;
  height: 100vh;
  padding-bottom: 0;
}

.video-player-container:fullscreen .video-wrapper {
  width: 100vw;
  height: 100vh;
  padding-bottom: 0;
}

.video-player-container:-webkit-full-screen .responsive-video {
  object-fit: contain;
}

.video-player-container:fullscreen .responsive-video {
  object-fit: contain;
}

/* Cambiar icono en pantalla completa */
.video-player-container:-webkit-full-screen .fullscreen-enter,
.video-player-container:fullscreen .fullscreen-enter {
  display: none;
}

.video-player-container:-webkit-full-screen .fullscreen-exit,
.video-player-container:fullscreen .fullscreen-exit {
  display: block;
}

/* Responsive para móviles */
@media (max-width: 768px) {
  .video-wrapper {
    padding-bottom: 75%; /* Relación 4:3 para móviles */
  }
  
  .custom-controls-overlay {
    bottom: 10px;
    right: 10px;
  }
  
  .fullscreen-toggle {
    width: 45px;
    height: 45px;
  }
  
  .fullscreen-toggle svg {
    width: 20px;
    height: 20px;
  }
  
  .video-loading span {
    font-size: 14px;
  }
}

/* Para tablets */
@media (min-width: 769px) and (max-width: 1024px) {
  .video-wrapper {
    padding-bottom: 60%; /* Relación intermedia */
  }
}

/* Para orientación landscape en móviles */
@media (max-width: 768px) and (orientation: landscape) {
  .video-wrapper {
    padding-bottom: 56.25%; /* Volver a 16:9 en landscape */
  }
  
  .custom-controls-overlay {
    bottom: 5px;
    right: 5px;
  }
  
  .fullscreen-toggle {
    width: 40px;
    height: 40px;
  }
  
  .fullscreen-toggle svg {
    width: 18px;
    height: 18px;
  }
}

/* Optimización para escritorio grande */
@media (min-width: 1200px) {
  .video-player-container {
    max-width: 1200px;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  }
  
  .video-wrapper {
    border-radius: 12px;
  }
}

/* Para videos verticales (detectar y ajustar dinámicamente) */
.video-vertical .video-wrapper {
  padding-bottom: 177.78%; /* Relación 9:16 para videos verticales */
}

/* Asegurar que el video sea siempre visible */
video::-webkit-media-controls {
  opacity: 0.8;
  transition: opacity 0.3s;
}

video:hover::-webkit-media-controls {
  opacity: 1;
}
</style>

<script>
// Variables globales
let isFullscreen = false;
let videoAspectRatio = 16/9; // Por defecto

// Ajustar relación de aspecto basado en las dimensiones reales del video
function adjustVideoAspect() {
  const video = document.getElementById('main-video');
  const wrapper = document.querySelector('.video-wrapper');
  
  if (video.videoWidth && video.videoHeight) {
    videoAspectRatio = video.videoWidth / video.videoHeight;
    
    // Si el video es vertical (relación < 1)
    if (videoAspectRatio < 1) {
      wrapper.style.paddingBottom = `${(1 / videoAspectRatio) * 100}%`;
      wrapper.classList.add('video-vertical');
    } else {
      // Para videos horizontales
      wrapper.style.paddingBottom = `${(1 / videoAspectRatio) * 100}%`;
    }
    
    console.log(`Video ajustado a relación: ${videoAspectRatio.toFixed(2)}:1`);
  }
}

// Pantalla completa
function toggleFullScreen() {
  const container = document.querySelector('.video-player-container');
  const video = document.getElementById('main-video');
  
  if (!isFullscreen) {
    if (container.requestFullscreen) {
      container.requestFullscreen();
    } else if (container.webkitRequestFullscreen) {
      container.webkitRequestFullscreen();
    } else if (container.mozRequestFullScreen) {
      container.mozRequestFullScreen();
    } else if (container.msRequestFullscreen) {
      container.msRequestFullscreen();
    }
  } else {
    if (document.exitFullscreen) {
      document.exitFullscreen();
    } else if (document.webkitExitFullscreen) {
      document.webkitExitFullscreen();
    } else if (document.mozCancelFullScreen) {
      document.mozCancelFullScreen();
    } else if (document.msExitFullscreen) {
      document.msExitFullscreen();
    }
  }
}

// Manejar eventos de pantalla completa
function handleFullscreenChange() {
  const container = document.querySelector('.video-player-container');
  const video = document.getElementById('main-video');
  
  isFullscreen = !!(document.fullscreenElement || 
                    document.webkitFullscreenElement || 
                    document.mozFullScreenElement || 
                    document.msFullscreenElement);
  
  // Optimizar para pantalla completa
  if (isFullscreen) {
    // Pausar y reanudar para forzar redimensionamiento en algunos navegadores
    const wasPlaying = !video.paused;
    if (wasPlaying) {
      video.pause();
      setTimeout(() => video.play(), 100);
    }
  }
}

// Mostrar/ocultar indicador de carga
function setupVideoLoading() {
  const video = document.getElementById('main-video');
  const loadingIndicator = document.getElementById('loading-indicator');
  
  video.addEventListener('waiting', () => {
    loadingIndicator.style.display = 'flex';
  });
  
  video.addEventListener('canplay', () => {
    loadingIndicator.style.display = 'none';
  });
  
  video.addEventListener('playing', () => {
    loadingIndicator.style.display = 'none';
  });
}

// Detectar cambios de orientación en móviles
function handleOrientationChange() {
  setTimeout(adjustVideoAspect, 100);
}

// Inicialización
document.addEventListener('DOMContentLoaded', function() {
  // Configurar eventos
  document.addEventListener('fullscreenchange', handleFullscreenChange);
  document.addEventListener('webkitfullscreenchange', handleFullscreenChange);
  document.addEventListener('mozfullscreenchange', handleFullscreenChange);
  document.addEventListener('MSFullscreenChange', handleFullscreenChange);
  
  // Configurar carga del video
  setupVideoLoading();
  
  // Detectar orientación
  window.addEventListener('orientationchange', handleOrientationChange);
  window.addEventListener('resize', handleOrientationChange);
  
  // También permitir pantalla completa con doble click
  document.getElementById('main-video').addEventListener('dblclick', toggleFullScreen);
  
  // Ajustar cuando el video esté listo
  const video = document.getElementById('main-video');
  if (video.readyState >= 1) {
    adjustVideoAspect();
  }
});

// Fallback para navegadores antiguos
function requestFullScreenFallback(element) {
  if(element.requestFullscreen) {
    element.requestFullscreen();
  } else if(element.mozRequestFullScreen) {
    element.mozRequestFullScreen();
  } else if(element.webkitRequestFullscreen) {
    element.webkitRequestFullscreen();
  } else if(element.msRequestFullscreen) {
    element.msRequestFullscreen();
  }
}

// Forzar redimensionamiento en carga
window.addEventListener('load', function() {
  setTimeout(adjustVideoAspect, 500);
});
</script>
{{< /raw >}}



[&#8592;]({{< ref "_index.md" >}})
