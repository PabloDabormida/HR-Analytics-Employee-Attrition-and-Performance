# HR-Analytics-Employee-Attrition-and-Performance

<br>

📄 **Documentacion Completa Disponible**

Este Readme.md presenta un resumen del análisis. Para acceder a la documentación completa, incluyendo metodología, análisis detallado, insights y recomendaciones finales, consulta el siguiente documento:
📎 **[Descargar Documentacion (PDF)](https://github.com/PabloDabormida/HR-Analytics-Employee-Attrition-and-Performance/blob/main/Documentacion.pdf)**
<br>
<br>

## 1. Resumen General:
   
El objetivo de este informe es analizar la rotación de empleados. La rotación se describe
como la pérdida gradual de empleados a lo largo del tiempo. Este fenómeno representa un
problema importante para todas las organizaciones, ya que puede tener implicaciones en el
personal, la moral de los empleados, los costos de los proyectos, la pérdida de experiencia y,
en general, un obstáculo para el crecimiento organizacional. Examinaremos los factores más
importantes que influyen en la rotación dentro de una organización. Consideraremos si estos
factores están bajo el control de la organización y qué acciones se pueden utilizar para mitigar
o combatir la rotación. También analizaremos las tendencias actuales en Recursos Humanos y
cómo estas se aplican a nuestro análisis; finalmente, con base en nuestros resultados,
concluiremos con ideas y recomendaciones.
<br>
<br>
## 2. Introducción:
   
El capital humano es uno de los mayores activos que una organización puede poseer.
Las empresas pueden gastar hasta un 70% de los costos totales del negocio en empleados. Estos
costos incluyen salarios, formación, reclutamiento e inversiones en habilidades. Además,
reclutar y retener talento destacado es fundamental para el crecimiento y la viabilidad a largo
plazo de cualquier empresa. A menudo, los empleados poseen características clave que son
instrumentales para impulsar a la empresa hacia adelante. Sabiendo esto, cuando los empleados
deciden renunciar o dejar una compañía, puede convertirse en un problema serio. Con cada
empleado, la empresa pierde su inversión directa junto con todo el conocimiento y la
experiencia que el empleado habría proporcionado de forma inherente. En el campo de
Recursos Humanos, cuando los empleados deciden abandonar la empresa, esto se conoce como
pérdida de personal, y este es el foco de nuestro análisis.3
Al analizar más a fondo las causas de la deserción, vemos que hay evidencias
superpuestas de por qué los empleados deciden irse, donde en la mayoría de los casos se debe a
las siguientes razones: remuneración insatisfactoria, beneficios insatisfactorios, falta de
oportunidades de crecimiento o desarrollo, problemas con el equilibrio entre el trabajo y la vida
personal, mala gestión, malas condiciones de trabajo y falta de reconocimiento por los logros
laborales o el valor agregado en el lugar de trabajo.
En este informe, analizaremos la validez de estas razones a través de un análisis exhaustivo de
un conjunto de datos de empleados disponible públicamente. El enfoque que seguiremos se basa
en un conjunto de procedimientos. Estos procedimientos son los siguientes: investigación,
análisis exploratorio de datos, manipulación y limpieza de datos, preparación del modelo,
construcción y evaluación de modelos, y finalmente, visualización y análisis de datos utilizando
Power BI.

• **Investigación Inicial:** Comenzaremos con una revisión del conjunto de datos para
comprender su estructura, las variables disponibles y su relevancia con respecto a los objetivos
del análisis. Esta etapa es fundamental para establecer el alcance del proyecto y anticipar posibles
desafíos.

• **Manipulación y Limpieza de Datos:** A continuación, procederemos a limpiar el
conjunto de datos, abordando valores faltantes, duplicados y errores en los datos. Este paso
garantiza que los datos sean confiables y estén listos para ser utilizados en análisis posteriores.

• **Normalizacion de Datos:** Una vez que los datos estén limpios, los normalizaremos para
asegurar que estén en un formato adecuado para el modelado. Esto incluye la transformación de
variables y la codificación de datos categóricos.

• **Construcción del Modelo Relacional:** Después de la normalización, procederemos a
diseñar el modelo relacional, creando un diagrama entidad-relación (ER) que represente las
relaciones entre las diferentes entidades en el conjunto de datos. Esto proporciona una base
sólida para consultas estructuradas y análisis detallados.

• **Análisis Exploratorio de Datos (EDA):** Se realiza un análisis descriptivo preliminar
para identificar patrones, tendencias y anomalías en los datos. Mediante el uso de
visualizaciones básicas, se obtiene una comprensión inicial de las relaciones clave entre las
variables.

• **Análisis y Visualización de Datos:** Finalmente, realizaremos un análisis detallado
utilizando el modelo relacional como guía, y utilizaremos Power BI para crear visualizaciones
interactivas que resalten patrones clave y faciliten la interpretación de los resultados. Esto nos
permitirá presentar hallazgos clave de manera clara y efectiva.
<br>
<br>
## 3. Descripción General de los Datos

El núcleo de nuestro análisis deriva de un conjunto de datos disponible públicamente,
que proporciona variables similares a las que tendría a disposición el personal típico de
Recursos Humanos. Este conjunto de datos se puede encontrar en Kaggle como "HR
Analytics Employee Attrition & Performance"(Fuente: https://www.kaggle.com/datasets/mahmoudemadabdallah/hr-analytics-employee-attrition-and-performance). Está
compuesto por más de mil cuatrocientas observaciones y treinta y cinco columnas.
Dentro del conjunto de datos, tenemos una combinación de tipos de datos numéricos y
categóricos. Algunos ejemplos de tipos de datos numéricos incluyen la edad del empleado,
sus ingresos mensuales y los años que lleva trabajando.en la empresa.Como ejemplos de
variables categóricas tenemos la educación, el género, el puesto de trabajo o el departamento
en el que trabaja el empleado.Es importante verificar la construcción del conjunto de datos
y sus tipos de variables, ya que la composición de los datos influye directamente en la
naturaleza de lo que es posible en el proceso de análisis.
<br>
<br>
## 4. Procesamiento de los Datos
### 4.1. Conversión del archivo CSV a tabla estructurada
El análisis partió de un archivo CSV. Aunque el archivo se identificaba como .csv, tenía la
extensión .xls, lo que fue corregido abriéndolo en Excel y guardándolo como archivo .csv
auténtico. Esto permitió asegurar que los datos pudieran ser procesados correctamente en
Power BI.
Posteriormente, el archivo fue convertido a una tabla estructurada en Excel para facilitar la
manipulación de datos. Esta conversión permitió aplicar filtros, ordenar datos y realizar
operaciones en columnas específicas de manera eficiente.
<br>
<br>
### 4.2. Eliminación de columnas innecesarias
Se revisaron las columnas del dataset y se eliminaron aquellas que no aportaban valor
directo al análisis planteado. Por ejemplo, campos irrelevantes como EmployeeCount,,
EmployeeNumber o cualquier dato que no estuviera relacionado con el desempeño o la
satisfacción laboral. Esta reducción de columnas no solo simplificó el modelo de datos, sino
que también mejoró el rendimiento del análisis al disminuir la complejidad.
<br>
<br>
### 4.3. Verificación de duplicados
Se revisaron los datos para identificar y eliminar duplicados en campos que deberían
contener valores únicos, como EmployeeID. Esto fue necesario para garantizar la integridad
de los datos y evitar inconsistencias en el análisis posterior.
<br>
<br>
### 4.4. Creación de la tabla "Performances"
Se diseñó una tabla independiente llamada "Performances" que agrupa todos los datos
numéricos relacionados con la satisfacción y desempeño del empleado. Esto incluyó
indicadores como:

• **JobSatisfaction**

• **WorkLifeBalance**

• **EnvironmentSatisfaction**

• **RelationshipSatisfaction**

• **WorkLifeBalance**

• **JobInvolvement**

<br>
Esta decisión tuvo varias justificaciones:

- Estandarización: Centralizar todos los indicadores numéricos en una única tabla
facilita la visualización de las métricas de desempeño.

- Optimización del modelo: Al separar los datos cuantitativos de los descriptivos,
se creó una estructura más clara y eficiente para el análisis en Power BI.

- Escalabilidad: Permite agregar nuevas métricas relacionadas al desempeño en el
futuro sin modificar otras tablas.
<br>

### 4.5. Creación del campo PerformanceID
<br>

Para identificar de manera única cada registro en la tabla "Performances", se generó un
campo denominado PerformanceID. Este campo fue construido utilizando una fórmula
en Excel:

**= "PR" & FILA() - FILA(1)**

Esta fórmula genera un identificador único para cada fila, con un formato del tipo PR1,
PR2, ..., PR140. Esto no solo permitió enlazar la tabla "Performances" con otras tablas
del modelo, sino que también aseguró la trazabilidad de cada registro.
4.5. Creación del campo PerformanceID

También se agrego el EmployeeID , campo por el cual se creara la relación con la tabla
Employees.
<br>
<br>
### 4.6. Creación de tablas separadas para indicadores específicos

Con base en los indicadores de desempeño y satisfacción, se crearon tablas
independientes para cada uno de los aspectos evaluados, como:

• **JobSatisfaction:** Contiene los niveles descriptivos de satisfacción laboral.

• **EnvironmentSatisfactionLevel:** Define el nivel de satisfacción con el
ambiente laboral.

• **WorkLifeBalanceLevel**: Clasifica las puntuaciones de equilibrio entre vida y trabajo.

• **RelationshipSatisfactionLevel:** Define el nivel de satisfacción entre el empleado y
el empleador.

• **PerformanceRating:** Describe el rating del empleado basado en su performance en
el trabajo segun su manager.

• **JobInvolvemente:** Define el nivel de compromiso del empleado con el trabajo.
<br>
<br>
Este enfoque tuvo las siguientes ventajas:

**Legibilidad:** Al separar las categorías descriptivas de los valores numéricos, el modelo
se volvió más comprensible.
**Flexibilidad:** Permite realizar cálculos y consultas de manera específica para cada
indicador sin afectar las demás métricas.
**Estandarización:** Las tablas separadas facilitan la reutilización de las categorías
descriptivas en otros análisis o reportes.

## 5. Alcance
El análisis incluirá la recopilación, almacenamiento y análisis de datos relacionados con el
desempeño (evaluaciones de rendimiento), satisfacción (niveles de satisfacción en distintos
aspectos) y nivel educativo de cada empleado. También se investigarán factores como balance
vida-trabajo, antigüedad, y oportunidades de capacitación. Este análisis servirá para entender
patrones y tendencias en el desarrollo de los empleados y su satisfacción, con el fin de hacer
recomendaciones para mejorar el rendimiento y retener al talento.
<br>
<br>
#### **Nivel Estratégico**
Este análisis permitirá a los líderes organizacionales tomar decisiones informadas para:

• Diseñar estrategias de retención enfocadas en los empleados de alto desempeño y aquellos
en riesgo de abandono.

• Identificar áreas críticas que afectan el compromiso de los empleados, como la gestión
gerencial, el entorno laboral y las oportunidades de desarrollo.
<br>
<br>
#### **Nivel Táctico**
En un nivel más operativo, los resultados de este análisis servirán para:
• Priorizar iniciativas de capacitación y desarrollo basadas en las áreas donde se
identifiquen brechas de desempeño.

• Optimizar procesos de evaluación de desempeño y satisfacción para asegurar una
alineación con los objetivos estratégicos de la organización.
<br>
<br>
#### **Nivel Operativo**
Finalmente, el proyecto impactará a nivel de implementación en:

• Creación de programas personalizados de capacitación y mentoría.

• Ajustes específicos en políticas de trabajo, como esquemas híbridos o soporte para
empleados con largas distancias al trabajo.
<br>
<br>

## 6. Hipótesis

Los empleados con mayor satisfacción laboral y balance entre vida laboral y personal tienden a
permanecer más tiempo en la empresa, lo que reduce la tasa de otación (attrition) en
comparación con aquellos que reportan menor satisfacción en estos aspectos.
Este análisis buscará evaluar la relación entre la satisfacción laboral y la deserción laboral
utilizando análisis multivariables. Se segmentarán los datos de acuerdo a diferentes
departamentos y se realizarán análisis de regresión logística para identificar los factores más
influyentes en la rotación de empleados. Además, se buscarán patrones en la antigüedad y las
promociones para determinar su relación con la satisfacción y la retención.
<br>
<br>

## 7. Herramientas
• Excel para la lectura, limpieza y normalizacion de los datos.

• PowerPoint para la creación del diseño del mockup.

• Miro para la creación del diagrama entidad-relación (https://miro.com/).

• Power BI para la crreacion del dashboard.
<br>
<br>

## 8. Conclusiones

#### Factores Críticos de Rotación:

• **Sales Representative:** Este rol presenta la mayor tasa de rotación.

• **Stock Option Level:** Los empleados con nivel 0 tienen significativamente mayor
rotación (65 % de los que abandonaron la empresa).

• **OverTime:** Los empleados que realizan horas extra tienen una rotación mucho mayor
(30,53 %).

• **Business Travel:** Los empleados que viajan frecuentemente tienen una tasa de rotación
del 24,91 %.43

• **Monthly Income:** Más del 47 % de los empleados que abandonan la empresa tienen
salarios inferiores a $3,000.
<br>
<br>
#### Segmentación por Perfil Demográfico:
• Los empleados jóvenes (<35 años) presentan las tasas de rotación más altas.

• Los empleados solteros tienen mayor probabilidad de rotación.
<br>
<br>
#### Satisfacción y Balance Laboral:
• Bajos niveles de Job Satisfaction, Environment Satisfaction, WorkLife Balance y
Relationship Satisfaction están asociados con mayores tasas de rotación.

En resumen, los resultados confirman que los niveles de satisfacción y el balance entre
vida laboral y personal son determinantes clave en la retención de empleados. Además,
factores como salarios competitivos, planes de carrera y una mejor gestión del talento
joven deben ser prioridad para reducir la rotación.
<br>
<br>
## 9. Recomendaciones

##### Incentivos Económicos
• **Stock Options:** Introducir planes desde el inicio para roles críticos.

• **Salarios Competitivos:** Ajustar los rangos salariales por debajo de $3,000 para
reducir la rotación.
<br>
<br>
#### Desarrollo de Carrera
• Establecer programas de desarrollo profesional, especialmente para roles con alta
rotación como Sales Representative.

• Implementar estrategias para reducir la rotación temprana en los primeros años.
Flexibilidad y Beneficios.

• Ofrecer opciones de trabajo remoto y horarios flexibles para empleados con alta
carga de viajes laborales.
<br>
<br>
#### Relación con Managers
• Capacitar a los gerentes para mejorar la retención en los primeros años y tras largos
periodos de supervisión.
<br>
<br>
#### Mejora de Satisfacción Laboral
• Diseñar programas que fomenten el balance entre vida laboral y personal.

• Mejorar las condiciones del entorno laboral para incrementar la satisfacción general.

<br>

---
📄**Para un análisis detallado, accede al informe completo.**
📎 **[Descargar Documentacion (PDF)](https://github.com/PabloDabormida/HR-Analytics-Employee-Attrition-and-Performance/blob/main/Documentacion.pdf)**

