+++
title = "Mapa"
+++

[&#8592;]({{< ref "_index.md" >}})

# Mapa

**📍 Hackmeeting Bolivia 0x7e9**  
**🏛️ UAGRM - F.I.C.C.T.**  
**🏢 Módulo 236, Salón Auditorio (4to piso)**  
**🗓️ 5 y 6 de Diciembre**

Usa el mapa para llegar a la ubicación.

{{< raw >}}

<style>
  /* Contenedor general responsive */
  .hm-responsive-wrapper {
    width: 100%;
    overflow-x: auto; /* Por si el contenido es muy grande */
  }

  /* La tabla ocupará 100% en móvil */
  .hm-responsive-table {
    width: 100%;
    max-width: 800px;
    border: 5px solid #ff00ff;
    border-radius: 15px;
    margin: 20px auto;
    background: linear-gradient(135deg, #ffccf9, #ff66ff);
    padding: 10px;
    box-shadow: 0 4px 8px rgba(255, 0, 255, 0.3);
    border-collapse: collapse;
  }

  /* En pantallas pequeñas, las columnas se apilan */
  @media (max-width: 650px) {
    .hm-responsive-table tr {
      display: flex;
      flex-direction: column;
    }

    .hm-responsive-table td {
      border-right: none !important;
      border-radius: 10px !important;
      margin-bottom: 10px;
    }

    /* Asegurar que el iframe sea 100% */
    .hm-map iframe {
      width: 100% !important;
      height: 250px !important;
    }
  }
</style>

<div class="hm-responsive-wrapper">
<table class="hm-responsive-table">
  <tr>
    <td style="
        padding: 15px;
        border-right: 2px solid #ff00ff;
        background: rgba(255, 255, 255, 0.9);
        border-radius: 10px 0 0 10px;
        text-align: center;
        vertical-align: middle;
        font-family: Arial, sans-serif;
        font-size: 14px;
        line-height: 1.5;
    ">
      <br>Universidad Autónoma Gabriel René Moreno<br>
      F.I.C.C.T. - Modulo 236 - Salón auditorio<br>
      <br>
    </td>

    <td class="hm-map" style="
        padding: 10px;
        background: rgba(255, 255, 255, 0.9);
        border-radius: 0 10px 10px 0;
        text-align: center;
    ">
      <iframe 
        width="450" 
        height="350" 
        frameborder="0" 
        scrolling="no" 
        marginheight="0" 
        marginwidth="0" 
        src="https://www.openstreetmap.org/export/embed.html?bbox=-63.1969960%2C-17.7772100%2C-63.1929960%2C-17.7752100&amp;layer=mapnik&amp;marker=-17.7762100%2C-63.1949960"
        style="border-radius: 8px; width: 100%; max-width: 450px;"
      ></iframe>

      <br/>
      <small>
        <a href="https://www.openstreetmap.org/#map=19/-17.776210/-63.194996" target="_blank">
          Ver mapa más grande
        </a>
      </small>
    </td>
  </tr>
</table>
</div>

{{< /raw >}}


[&#8592;]({{< ref "_index.md" >}})
