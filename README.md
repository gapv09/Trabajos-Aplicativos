# AEIOU
Inferencia de Correlación
Paredes Valerio Gustavo
2023-03-04
#Llamar a la base de datos

library(readxl)
Libro2 <- read_excel("C:\\Users\\guspv\\OneDrive\\Desktop\\Libro2.xlsx")
View(Libro2)
#Diagrama de dispersión entre las variables: mortalidad infantil, madres analfabetas en % y economia promedio de ingreso.

plot(Libro2)


#Para las variables Mortalidad infantil (y) y madres analfabetas (x)

#Coeficiente de Correlación

n<-16
xy<-27808
sy<-778
sx<-452
xx<-16528
yy<-56268
(n*xy-sy*sx)/sqrt((n*xx-sx^2)*(n*yy-sy^2))
## [1] 0.7002308
r<-0.7002308
r=0.7002308=70.0023% ; Significa que existe una relación lineal fuerte entre las variables.

#Coeficiente de Determinante

r^2
## [1] 0.4903232
R=0.4903232=49.03% ; se refiere a la variable mortalidad infantil es explicado por las madres analfabetas.

#Inferencia de correlación con un nivel de significancia de 1%

#1)Hipótesis:

Ho: p=0 ; (No existe relación entre la mortalidad infantil y las madres analfabetas)

H1: p diferente de 0 ; (Existe relación entre la mortalidad infantil y las madres analfabetas)

#2)Valor Crítico: gl=16 ; (1-a/2)=0.995

tt<-2.947
#3)Estadístico:

r*sqrt((n-2)/1-r^2)
## [1] 2.573734
tc<-2.573734
#4)Decisión: |tc|<tt -> |2.57|<2.94 ; se acepta la hipótesis nula (Ho).

#5)Conclusión: Se concluye que estadísticamente no hay evidencia suficiente para indicar que el coeficiente de correlación es significativo, no existe relación entre la mortalidad infantil y las madres analfabetas. Para un nivel de significancia de 1%.

#Para las variables Mortalidad infantil (y) y economia promedio de ingreso (xa)

#Coeficiente de Correlación

n<-16
xay<-45623
sy<-778
sxa<-1030
xaxa<-73838
yy<-56268
(n*xay-sy*sxa)/sqrt((n*xaxa-sxa^2)*(n*yy-sy^2))
## [1] -0.3785349
r1=-0.3785349
r1=-0.3785349=-37.85% ; Significa que existe una relación lineal negativa débil entre las variables.

#Coeficiente de Determinante

r1^2
## [1] 0.1432887
R1=0.1432887=14.32% ; se refiere a la variable mortalidad infantil es explicado por la economia promedio de ingreso.

#Inferencia de correlación con un nivel de significancia de 1%

#1)Hipótesis:

Ho: p=0 ; (No existe relación entre la mortalidad infantil y economia promedio de ingreso)

H1: p diferente de 0 ; (Existe relación entre la mortalidad infantil y economia promedio de ingreso)

#2)Valor Crítico: gl=16 ; (1-a/2)=0.995

tt<-2.947
#3)Estadístico:

r1*sqrt((n-2)/1-r1^2)
## [1] -1.409081
tc<--1.409081
#4)Decisión: |tc|<tt -> |-1.40|<2.94 ; se acepta la hipótesis nula (Ho).

#5)Conclusión: Se concluye que estadísticamente no hay evidencia suficiente para indicar que el coeficiente de correlación es significativo, no existe relación entre la mortalidad infantil y economia promedio de ingreso. Para un nivel de significancia de 1%.

#Correlación para las 3 variables

rr1=-0.1669834
(((r)^2+(r1)^2-2*r*r1*rr1)/(1-(rr1)^2))^(1/2)
## [1] 0.7488157
El coeficiente de correlación: 74.88% , existe una correlación alata entres las variables: mortalidad infantil, madres analfabetas y economia promedio de ingreso.
