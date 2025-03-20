
```leaflet  
### Tutorial: [https://youtu.be/54EyMzJP5DU](https://youtu.be/54EyMzJP5DU)  
### id dever ser único
id: Mapa_Generico
### Trave os Pins para que não sejam movidos
lock: true  
### Se marcado com otrue, a visualização do mapa vai recentralizar a medida que você afastar o zoom.  
recenter: true  
### Se true, desativa a rolagem do mouse para aumentar e diminuir o zoom em um mapa. Os controles dos botões ainda funcionam. 
noScrollZoom: true  
image: [[HighRes (with Saltmarsh) (Orig).jpg]]  
### Altura do pixel do mapa x 1 / (pixels entre a escala da barra / 100) 
### Largura do pixel do mapa x 1 / (pixels entre a escala da barra / 100)  
### Observe que esta fórmula requer ajustes dependendo do seu mapa. A ideia é determinar o número de unidades entre a régua de media. Dividimos aqui por 100 porque minha régua de medida mede 100 unidades. Se a régua de medidas do seu mapa mede em unidades de 50, você deve dividir por 50. A ideia é calcular quantos pixels equivalem a 1 unidade.  
### Os Bounds: limites são inseridos como [Altura, Largura]  
bounds: [[0,0], [1815.07, 2805.48]]  
height: 900px  
width: 95%  
### Isso define onde o mapa começa por padrão. Defina-o no meio (metade) dos seus limites.
lat: 907.53  
long: 1402.74  
### 0 é sem zoom. O zoom negativo se afasta do mapa. O zoom positivo avança em direção ao mapa.
minZoom: -1.5  
### O zoom máximo é 18.  
maxZoom: 1.5  
### Passe o mouse sobre o ícone Redefinir zoom para ver seu nível de zoom atual.
defaultZoom: -1  
### Até que ponto o zoom aumenta ou diminui em cada etapa. Pode estar em decimais. 
zoomDelta: 0.5  
### Esta é uma string, então pode ser qualquer texto. Altere-o para corresponder à unidade de medida do seu mapa.
unit: kilometros  
scale: 1  
darkMode: false  
```