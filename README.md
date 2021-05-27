# Trabajo-2-Datos-Hidrol-gicos-
# Tarea 2 Datos Hidrológicos 

inp <- read.csv("FDC.csv" , na.strings = "")

head(inp)
dim(inp)

#Volumen de agua por series de tiempo entre el río Estrella y río Banano 

### En este caso se realiza una comparación entre los ríos estrella y banano, con el fin de determinar el volumen de agua que posee cada uno, a lo largo de cierto periodo.

plot(inp[ ,2], type = "l", col= "orange", 
     main = 'Volumen de agua por series de tiempo entre el río Estrella y río Banano', 
     xlab = 'Banano',
     ylab = 'Estrella'
     )
             
lines(inp[ ,3], col="blue")

# Histograma 
### En este gráfico se presenta una distribución de la frecuencia con respecto a las crecidas en el caudal del río estrella y río banano
summary(inp[ ,2:3])
hist(inp[ ,2], col = "green", main = 'Histograma Río Estrella', xlab = 'caudal río Estrella')
hist(inp[ ,3], col = "purple", main = 'Histograma Río Banano', xlab = 'Caudal río Banano')
