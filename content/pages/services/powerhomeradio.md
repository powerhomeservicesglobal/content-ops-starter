---
type: PageLayout
title: Powerhome Radio
sections:
  - type: CarouselSection
    items:
      - type: FeaturedItem
        title: 'Transmisión más Reciente '
        tagline: Más Reciente
        subtitle: Increase your reach
        text: >-
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae.
          explicabo.
        image:
          type: ImageBlock
          url: /images/img-placeholder.svg
          altText: Featured item
          styles:
            self:
              borderRadius: medium
        actions: []
        colors: bg-neutralAlt-fg-dark
        styles:
          self:
            padding:
              - pt-9
              - pb-9
              - pl-9
              - pr-9
            textAlign: left
            borderRadius: large
            flexDirection: row
            justifyContent: center
      - type: FeaturedItem
        title: ''
        tagline: Otros Episodios
        subtitle: Be in good company
        text: |+


          <meta charset="UTF-8">
              <meta name="viewport" content="width=device-width, initial-scale=1.0">
              <title>Powerhome Radio</title>
              <style>
                  body {
                      background-color: #111;
                      color: #fff;
                      font-family: Arial, sans-serif;
                      text-align: center;
                  }

                  .video-container {
                      position: relative;
                      display: inline-block;
                      width: 560px;
                      height: 315px;
                  }

                  iframe {
                      border: none;
                      width: 100%;
                      height: 100%;
                  }

                  .nav-arrow {
                      position: absolute;
                      top: 50%;
                      transform: translateY(-50%);
                      background-color: rgba(0, 0, 0, 0.7);
                      border: none;
                      color: #fff;
                      padding: 10px;
                      font-size: 2em;
                      cursor: pointer;
                      z-index: 10;
                      border-radius: 50%;
                  }

                  .nav-left {
                      left: -60px;
                  }

                  .nav-right {
                      right: -60px;
                  }

                  .nav-arrow:hover {
                      background-color: rgba(255, 255, 255, 0.5);
                  }

              </style>


              <h1>Powerhome Radio</h1>

              <div class="video-container">
                  
                  <button class="nav-arrow nav-left" onclick="previousVideo()">❮</button>
                  <iframe id="yt-player" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>
                  <button class="nav-arrow nav-right" onclick="nextVideo()">❯</button>
              </div>

              <script>
                  const playlistId = 'PLCJ3CD9TzNKkyoMRU-81f9RwUZK-d_4Hs';
                  const API_KEY = 'AIzaSyDIL1xNvU-z9g2fL6Rg5gc81vTQRKj89CY';
                  let currentIndex = 0;
                  let videoIds = [];

                  // Llamar a la API de YouTube para obtener la playlist
                  fetch(`https://www.googleapis.com/youtube/v3/playlistItems?part=snippet&playlistId=${playlistId}&maxResults=50&key=${API_KEY}`)
                      .then(response => response.json())
                      .then(data => {
                          videoIds = data.items.map(item => item.snippet.resourceId.videoId);
                          loadVideo(currentIndex);
                      })
                      .catch(error => console.error('Error al obtener la playlist:', error));

                  // Función para cargar el video actual
                  function loadVideo(index) {
                      const player = document.getElementById('yt-player');
                      player.src = `https://www.youtube.com/embed/${videoIds[index]}?autoplay=1`;
                  }

                  // Función para el video anterior
                  function previousVideo() {
                      if (currentIndex > 0) {
                          currentIndex--;
                          loadVideo(currentIndex);
                      }
                  }

                  // Función para el siguiente video
                  function nextVideo() {
                      if (currentIndex < videoIds.length - 1) {
                          currentIndex++;
                          loadVideo(currentIndex);
                      }
                  }
              </script>

        image:
          type: ImageBlock
          url: /images/img-placeholder.svg
          altText: Business consulting
          elementId: ''
          styles:
            self:
              borderRadius: medium
        actions: []
        colors: bg-dark-fg-light
        styles:
          self:
            padding:
              - pt-9
              - pb-9
              - pl-9
              - pr-9
            textAlign: left
            borderRadius: large
            flexDirection: row
            justifyContent: center
    variant: tabs-nav
    colors: bg-light-fg-dark
    styles:
      self:
        justifyContent: center
      subtitle:
        textAlign: center
slug: /services/powerhomeradio
isDraft: false
seo:
  type: Seo
  metaTitle: Landing Page
  metaDescription: Write here your new page's description including most relevant keywords.
  addTitleSuffix: true
  socialImage: /images/main-hero.jpg
  metaTags: []
---
