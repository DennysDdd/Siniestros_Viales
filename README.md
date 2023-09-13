<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº2** </h1>

# <h1 align=center>**<span style="color:silver">Siniestros viales en la Ciudad de Buenos Aires</span>**</h1>

<p align="center">
  <img src="src/caba.png" alt="ciudad"  width="50%"/>
</p>

### En este segundo proyecto individual, el desafío es encontrar insights referente a la información brindada por el Gobierno de Argentina en cuanto a accidentes viales en la Ciudad de Buenos Aires.
<br>
<div style="text-align: right; color: silver; font-size: 1.2em; font-weight: bold;">
  <a href="https://github.com/DennysDdd/Siniestros_Viales" style="color: silver; text-decoration: none;">
    by Dennys Diaz, Cohorte 13
  </a>
</div>

# <h1 align=center> **Intro** </h1>

Se obtiene información de los años 2016-2021 sobre los *homicidi#s* en la Ciudad de Buenos Aires(CABA), donde se detalla toda la información referente a esos sucesos, tales como ROL, el cual indica que papel desempeñaba la victima, asi también datos como la fecha y hora exacta, cantidad de victimas e incluso ubicación geográfica de los sucesos.

El presente trabajo tiene como finalidad mostrar de manera objetiva los **insights** obtenidos de los datos, apuntando a brindar sugerencias para evitar más trágicos desenlaces en la población de CABA. No es objetivo de este trabajo herir susceptibilidades.

# <h1 align=center> **Análisis de los datos**</h1>

Iniciamos observando la informacion en las hojas presentes en el archivo *homicidios.xlsx*, donde observaremos 4 hojas, de las cuales obtenemos información de los **HECHOS** en la hoja con el mismo nombre; así como información detallada sobre la víctimas del suceso en la hoja **VICTIMA**.

Observamos entonces la distribución de los datos en el siguiente mapa de calor:

<p align="center">
  <img src="src/distro_datos.png" alt="distro"  width="50%"/>
</p>

Posterior a la lectura de los datos procedemos a analizar en primer lugar la hoja de **HECHOS**, donde primero observaremos la distribución de los datos alrededor de los años en base al tipo de locación donde ocurrió el suceso. Para este y las consecuentes observaciones usaremos filtros en nuestas hojas ahora tomadas como dataframe en Jupyter Notebook de la siguiente manera:
```
DATAFRAME[DATAFRAME["COLUMNA A OBSERVAR"]]
```
Así obtenemos:

<p align="center">
  <img src="src/avenida.png" alt="avenida"  width="50%"/>
</p>

Pero que pasa si observamos la distribución de accidentes en todos los años, pero en base a las comunas de la data:

<p align="center">
  <img src="src/comuna.png" alt="comuna"  width="50%"/>
</p>

### **LA COMUNA 1 ES LA QUE PRESENTA MAYOR CANTIDAD DE VICTIMAS**

Ahora veamos la distribución de la hoja de **HECHOS** en relación al medio de trasnporte por el cual se desplazaba la victima, en el cual obtenemos la siguiente gráfica:

<p align="center">
  <img src="src/motos.png" alt="motos"  width="50%"/>
</p>

### **QUE INTERESANTE!**

Observamos que la mayor cantidad de víctimas son aquellas que se transportaban mediante **MOTOCICLETA**

Ahora que hemos observado la hoja de HECHOS, veamos que podemos observar en la hoja de **VICTIMAS**

A modo de recordatorio observaremos la información relevante de las columnas de la hoja VICTIMAS de la siguiente manera:
```
VICTIMAS[VICTIMAS["COLUMNA A OBSERVAR"]]
```
### **QUE ROL OCUPABAN LAS PERSONAS QUE PERECIERON EN LOS ACCIDENTES?**

Veamos la distribución:

<p align="center">
  <img src="src/rol2.png" alt="rol"  width="50%"/>
</p>

 ### **NO SOLO LAS PERSONAS QUE MANEJABAN ALGUN VEHICULO SON LAS VICTIMAS, OBSERVAMOS QUE MUCHOS DE LOS PEATONES TAMBIÉN FUERON AFECTADOS!**

Veamos otra consideración interesante de esta hoja:

<p align="center">
  <img src="src/sexo2.png" alt="sexo"  width="50%"/>
</p>

### **OBSERVAMOS QUE LA MAYOR CANTIDAD DE VICTIMAS SON DEL SEXO MASCULINO**

Hasta ahora hemos solo observado algunas columnas de las múltiples en cada una de las hojas, se ha realizado este análisis pues las columnas mostradas presentan en su totalidad variables de tipo categórica, las cuales facilitan la visualización de la distribución visual de la totalidad de los datos, además que van acorde a los objetivos de preparar la data para visuaiizar los KPI del presente trabajo.

Pero...

### **QUE KPIs VEREMOS?**

1. Reducir la tasa de homicidios con el objetivo de lograr una disminución del **10%**

2. Reducir la cantidad de accidentes mortales de motocicletas en **7%**

3. Reducir la cantidad de accidentes viales en la **COMUNA1** en **20%**


### Tasa de Homicidios semestral

* Se realizaron medidas calculadas semestrales en cada año para poder comparar el avance entre el segundo semestre VS el primero, con le objetivo de observar el aumento/disminución del mismo

### Tasa de accidentes mortales en motocicletas

* Se realizó una medida calculada de manera anual únicamente tomando en cuenta los accidentes de la hoja de VICTIMAS donde la categoría VICTIMA es MOTO, comparando dichas medidas entre 2 años consecutivos (Año presente vs Año anterior) con el objetivo de medir la tasa de crecimiento/descendo del mismo.

### Tasa de accidentes en la COMUNA 1

* Se realizó, de manera semejante a la tasa de mortandad en motocicletas, una comparativa anual entre la cantidad de accidentes, únicamente tomando en cuenta los sucesos en la COMUNA 1


# <h1 align=center> **Conclusiones y Recomendaciones**</h1>

Pudimos observar que existen muchísimos puntos a mejorar en cuanto a seguridad vial, por ejemplo en el caso de motocicletas, **REALMENTE LOS AFECTADOS LLEVABAN EL EQUIPO BÁSICO DE PROTECCIÓN (CASCO)**, sería interesante observar dicha información.

Se observó también que en la COMUNA 1 hay una disminución progresiva de la cantidad de accidentes, pero... Que tal si mejorarmos la señaletica e incluso nos apoyamos en los agentes policiales para poder reducir más del 17% que es el promedio en el cual va disminuyendo los accidentes.


# <h1 align=center> **Entregables**</h1>

## Índice de Archivos del Repositorio

+ [EDA Jupyter](EDA.ipynb)
+ [Información de los homicidios](homicidios.xlsx)
+ [Presentación de los siniestros](Siniestros_Viales(CABA).pbix)
+ [Carpeta con archivos complementarios](src)

## Fuentes de datos 

La fuente de donde se obtuvo la información en la que se basa el presente trabajo es:

+ [DATOS ARGENTINA](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales)