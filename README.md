# TP Visualización
## Tema: Spotify
DBD - ITBA - Visualización de la Información



## Objetivo

El objetivo de este trabajo fue visualizar mis escuchas de Spotify, tanto música como podcasts. El trabajo final se encuentra publicado [aquí](https://mpaulabonel.github.io/infovis/tp_spotify.html).




## Fuentes
Para este trabajo utilicé dos fuentes de datos: 

1. Información histórica de escuchas de Spotify (período: año previo). Para obtener estos datos es necesario realizar el pedido en esta [página](https://www.spotify.com/us/account/privacy/?_ga=2.184823009.998357364.1629131719-547053533.1604324023) con un tiempo de demora de algunos días a un mes.

2. Información de la API de Spotify extraída utilizando el paquete ['spotifyr'](https://www.rdocumentation.org/packages/spotifyr/versions/2.2.1) de R. Este paquete nos permite obtener información del artista y, fundamentalmente, de las canciones. Recurde que para acceder a estos datos es necesario previamente contar con una cuenta de [Spotify for developers](https://developer.spotify.com).


## Otros recursos útiles

Existen diversos tutoriales para comenzar a trabajar con estos datos. Yo trabajé con el siguiente [tutorial](https://towardsdatascience.com/explore-your-activity-on-spotify-with-r-and-spotifyr-how-to-analyze-and-visualize-your-stream-dee41cb63526).

El trabajo final fue realizado en Tableau. Otros recursos de utilidad para diagramar la visualización fueron los gráficos de [Flourish](https://public.flourish.studio/visualisation/7010328/) y las notebooks públicas de Observable sobre el tema. 

## Datos históricos 





## Algunos ejemplos de búsqueda usando 'spotifyr'

1. Establecer conexión con la API de Spotify:

<pre><code>
library(spotifyr)
Sys.setenv(SPOTIFY_CLIENT_ID = 'xxxxxxxx')
Sys.setenv(SPOTIFY_CLIENT_SECRET = 'xxxxxxxx')
get_spotify_authorization_code()
</code></pre>

2. Obtener características de las canciones pertenecientes a un artista:

<pre><code>
favArtist <- get_artist_audio_features(artist= 'xxxxxxxx')
</code></pre>

3. Obtener características de las canciones pertenecientes a una playlist:

<pre><code>
playlist_username <- 'xxxxxxxx'
playlist_uris <- c('xxxxxxxx')
playlist2020 <- get_playlist_audio_features(playlist_username, playlist_uris)
</code></pre>

