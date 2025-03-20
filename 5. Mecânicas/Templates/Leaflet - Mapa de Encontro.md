

```leaflet  
### Tutorial: [https://youtu.be/54EyMzJP5DU](https://youtu.be/54EyMzJP5DU)  
### o ID deve ser único 
id: nome_generico
image: [[MapName.png]]  
height: 1000px  
width: 70%  
### Isso define onde o mapa começa por padrão. Defina-o no meio (metade) dos seus bounds (limites).
lat: 50  
long: 50  
### 0 não é zoom. O zoom negativo se afasta do mapa. O zoom positivo avança em direção ao mapa.
minZoom: 0  
### O zoom máximo é 18. 
maxZoom: 18  
### Passe o mouse sobre o ícone Redefinir zoom para ver seu nível de zoom atual.
defaultZoom: 15  
### Até que ponto o zoom aumenta ou diminui em cada etapa. Pode estar em decimais. 
zoomDelta: 0.5  
### Esta é uma string, então pode ser qualquer texto. Altere-o para corresponder à unidade de medida do seu mapa.
unit: metros  
scale: 1  
darkMode: false  
```