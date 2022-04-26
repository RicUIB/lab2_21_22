---
title: "Taller datos FIFA 2019. Enunciado"
date: "25 marzo, 2022"
output:
  html_document: 
    toc: yes
    number_sections: yes
    keep_md: yes
  word_document:
    toc: yes
  pdf_document:
    toc: yes
    number_sections: yes
linkcolor: red
header-includes: \renewcommand{\contentsname}{Contenidos}
citecolor: blue
toccolor: blue
urlcolor: blue
---





# Taller evaluable datos FIFA 2020

Registraros en kaggle y bajaros  el data set [FIFA 2020  Datos completos 2015 a 2020](https://www.kaggle.com/stefanoleone992/fifa-20-complete-player-dataset).
Guarda los datos en una carpeta FIFA2020.

Las siguientes preguntas son relativas al data set `players_20.csv`. 

Hay que contestar con código R explicar muy brevemente cada salida. Subid a la activada el Rmd y el html. 


Rellenad estos datos:

**PONED NOMBRE**


*  Apellidos, Nombre Alumno 

## Pregunta 0

Explica  el data set y de qué tipo son cada una de las variables y  en qué tipo de  fichero están guardadas.  Carga los datos  en un data frame  con `read.csv` y explica las clases de cada columna de datos.  Explica  el parámeto `encoding`.


```r
datos = read.csv("FIFA2020/players_20.csv", encoding="UTF-8")
str(datos, 5)
```

```
## 'data.frame':	18278 obs. of  104 variables:
##  $ sofifa_id                 : int  158023 20801 190871 200389 183277 192985 192448 203376 177003 209331 ...
##  $ player_url                : chr  "https://sofifa.com/player/158023/lionel-messi/20/159586" "https://sofifa.com/player/20801/c-ronaldo-dos-santos-aveiro/20/159586" "https://sofifa.com/player/190871/neymar-da-silva-santos-jr/20/159586" "https://sofifa.com/player/200389/jan-oblak/20/159586" ...
##  $ short_name                : chr  "L. Messi" "Cristiano Ronaldo" "Neymar Jr" "J. Oblak" ...
##  $ long_name                 : chr  "Lionel Andrés Messi Cuccittini" "Cristiano Ronaldo dos Santos Aveiro" "Neymar da Silva Santos Junior" "Jan Oblak" ...
##  $ age                       : int  32 34 27 26 28 28 27 27 33 27 ...
##  $ dob                       : chr  "1987-06-24" "1985-02-05" "1992-02-05" "1993-01-07" ...
##  $ height_cm                 : int  170 187 175 188 175 181 187 193 172 175 ...
##  $ weight_kg                 : int  72 83 68 87 74 70 85 92 66 71 ...
##  $ nationality               : chr  "Argentina" "Portugal" "Brazil" "Slovenia" ...
##  $ club                      : chr  "FC Barcelona" "Juventus" "Paris Saint-Germain" "Atlético Madrid" ...
##  $ overall                   : int  94 93 92 91 91 91 90 90 90 90 ...
##  $ potential                 : int  94 93 92 93 91 91 93 91 90 90 ...
##  $ value_eur                 : int  95500000 58500000 105500000 77500000 90000000 90000000 67500000 78000000 45000000 80500000 ...
##  $ wage_eur                  : int  565000 405000 290000 125000 470000 370000 250000 200000 340000 240000 ...
##  $ player_positions          : chr  "RW, CF, ST" "ST, LW" "LW, CAM" "GK" ...
##  $ preferred_foot            : chr  "Left" "Right" "Right" "Right" ...
##  $ international_reputation  : int  5 5 5 3 4 4 3 3 4 3 ...
##  $ weak_foot                 : int  4 4 5 3 4 5 4 3 4 3 ...
##  $ skill_moves               : int  4 5 5 1 4 4 1 2 4 4 ...
##  $ work_rate                 : chr  "Medium/Low" "High/Low" "High/Medium" "Medium/Medium" ...
##  $ body_type                 : chr  "Messi" "C. Ronaldo" "Neymar" "Normal" ...
##  $ real_face                 : chr  "Yes" "Yes" "Yes" "Yes" ...
##  $ release_clause_eur        : int  195800000 96500000 195200000 164700000 184500000 166500000 143400000 150200000 92300000 148900000 ...
##  $ player_tags               : chr  "#Dribbler, #Distance Shooter, #Crosser, #FK Specialist, #Acrobat, #Clinical Finisher, #Complete Forward" "#Speedster, #Dribbler, #Distance Shooter, #Acrobat, #Clinical Finisher, #Complete Forward" "#Speedster, #Dribbler, #Playmaker  , #Crosser, #FK Specialist, #Acrobat, #Clinical Finisher, #Complete Midfield"| __truncated__ "" ...
##  $ team_position             : chr  "RW" "LW" "CAM" "GK" ...
##  $ team_jersey_number        : int  10 7 10 13 7 17 1 4 10 11 ...
##  $ loaned_from               : chr  "" "" "" "" ...
##  $ joined                    : chr  "2004-07-01" "2018-07-10" "2017-08-03" "2014-07-16" ...
##  $ contract_valid_until      : int  2021 2022 2022 2023 2024 2023 2022 2023 2020 2023 ...
##  $ nation_position           : chr  "" "LS" "LW" "GK" ...
##  $ nation_jersey_number      : int  NA 7 10 1 10 7 22 4 NA 10 ...
##  $ pace                      : int  87 90 91 NA 91 76 NA 77 74 93 ...
##  $ shooting                  : int  92 93 85 NA 83 86 NA 60 76 86 ...
##  $ passing                   : int  92 82 87 NA 86 92 NA 70 89 81 ...
##  $ dribbling                 : int  96 89 95 NA 94 86 NA 71 89 89 ...
##  $ defending                 : int  39 35 32 NA 35 61 NA 90 72 45 ...
##  $ physic                    : int  66 78 58 NA 66 78 NA 86 66 74 ...
##  $ gk_diving                 : int  NA NA NA 87 NA NA 88 NA NA NA ...
##  $ gk_handling               : int  NA NA NA 92 NA NA 85 NA NA NA ...
##  $ gk_kicking                : int  NA NA NA 78 NA NA 88 NA NA NA ...
##  $ gk_reflexes               : int  NA NA NA 89 NA NA 90 NA NA NA ...
##  $ gk_speed                  : int  NA NA NA 52 NA NA 45 NA NA NA ...
##  $ gk_positioning            : int  NA NA NA 90 NA NA 88 NA NA NA ...
##  $ player_traits             : chr  "Beat Offside Trap, Argues with Officials, Early Crosser, Finesse Shot, Speed Dribbler (CPU AI Only), 1-on-1 Rus"| __truncated__ "Long Throw-in, Selfish, Argues with Officials, Early Crosser, Speed Dribbler (CPU AI Only), Skilled Dribbling" "Power Free-Kick, Injury Free, Selfish, Early Crosser, Speed Dribbler (CPU AI Only), Crowd Favourite" "Flair, Acrobatic Clearance" ...
##  $ attacking_crossing        : int  88 84 87 13 81 93 18 53 86 79 ...
##  $ attacking_finishing       : int  95 94 87 11 84 82 14 52 72 90 ...
##  $ attacking_heading_accuracy: int  70 89 62 15 61 55 11 86 55 59 ...
##  $ attacking_short_passing   : int  92 83 87 43 89 92 61 78 92 84 ...
##  $ attacking_volleys         : int  88 87 87 13 83 82 14 45 76 79 ...
##  $ skill_dribbling           : int  97 89 96 12 95 86 21 70 87 89 ...
##  $ skill_curve               : int  93 81 88 13 83 85 18 60 85 83 ...
##  $ skill_fk_accuracy         : int  94 76 87 14 79 83 12 70 78 69 ...
##  $ skill_long_passing        : int  92 77 81 40 83 91 63 81 88 75 ...
##  $ skill_ball_control        : int  96 92 95 30 94 91 30 76 92 89 ...
##  $ movement_acceleration     : int  91 89 94 43 94 77 38 74 77 94 ...
##  $ movement_sprint_speed     : int  84 91 89 60 88 76 50 79 71 92 ...
##  $ movement_agility          : int  93 87 96 67 95 78 37 61 92 91 ...
##  $ movement_reactions        : int  95 96 92 88 90 91 86 88 89 92 ...
##  $ movement_balance          : int  95 71 84 49 94 76 43 53 93 88 ...
##  $ power_shot_power          : int  86 95 80 59 82 91 66 81 79 80 ...
##  $ power_jumping             : int  68 95 61 78 56 63 79 90 68 69 ...
##  $ power_stamina             : int  75 85 81 41 84 89 35 75 85 85 ...
##  $ power_strength            : int  68 78 49 78 63 74 78 92 58 73 ...
##  $ power_long_shots          : int  94 93 84 12 80 90 10 64 82 84 ...
##  $ mentality_aggression      : int  48 63 51 34 54 76 43 82 62 63 ...
##  $ mentality_interceptions   : int  40 29 36 19 41 61 22 89 82 55 ...
##  $ mentality_positioning     : int  94 95 87 11 87 88 11 47 79 92 ...
##  $ mentality_vision          : int  94 82 90 65 89 94 70 65 91 84 ...
##  $ mentality_penalties       : int  75 85 90 11 88 79 25 62 82 77 ...
##  $ mentality_composure       : int  96 95 94 68 91 91 70 89 92 91 ...
##  $ defending_marking         : int  33 28 27 27 34 68 25 91 68 38 ...
##  $ defending_standing_tackle : int  37 32 26 12 27 58 13 92 76 43 ...
##  $ defending_sliding_tackle  : int  26 24 29 18 22 51 10 85 71 41 ...
##  $ goalkeeping_diving        : int  6 7 9 87 11 15 88 13 13 14 ...
##  $ goalkeeping_handling      : int  11 11 9 92 12 13 85 10 9 14 ...
##  $ goalkeeping_kicking       : int  15 15 15 78 6 5 88 13 7 9 ...
##  $ goalkeeping_positioning   : int  14 14 15 90 8 10 88 11 14 11 ...
##  $ goalkeeping_reflexes      : int  8 11 11 89 8 13 90 11 9 14 ...
##  $ ls                        : chr  "89+2" "91+3" "84+3" "" ...
##  $ st                        : chr  "89+2" "91+3" "84+3" "" ...
##  $ rs                        : chr  "89+2" "91+3" "84+3" "" ...
##  $ lw                        : chr  "93+2" "89+3" "90+3" "" ...
##  $ lf                        : chr  "93+2" "90+3" "89+3" "" ...
##  $ cf                        : chr  "93+2" "90+3" "89+3" "" ...
##  $ rf                        : chr  "93+2" "90+3" "89+3" "" ...
##  $ rw                        : chr  "93+2" "89+3" "90+3" "" ...
##  $ lam                       : chr  "93+2" "88+3" "90+3" "" ...
##  $ cam                       : chr  "93+2" "88+3" "90+3" "" ...
##  $ ram                       : chr  "93+2" "88+3" "90+3" "" ...
##  $ lm                        : chr  "92+2" "88+3" "89+3" "" ...
##  $ lcm                       : chr  "87+2" "81+3" "82+3" "" ...
##  $ cm                        : chr  "87+2" "81+3" "82+3" "" ...
##  $ rcm                       : chr  "87+2" "81+3" "82+3" "" ...
##  $ rm                        : chr  "92+2" "88+3" "89+3" "" ...
##  $ lwb                       : chr  "68+2" "65+3" "66+3" "" ...
##  $ ldm                       : chr  "66+2" "61+3" "61+3" "" ...
##  $ cdm                       : chr  "66+2" "61+3" "61+3" "" ...
##  $ rdm                       : chr  "66+2" "61+3" "61+3" "" ...
##  $ rwb                       : chr  "68+2" "65+3" "66+3" "" ...
##   [list output truncated]
```

##  Pregunta 1

¿Qué 6  clubs tienen a los 10 mejores jugadores según la variable  "shooting"?




## Pregunta 2

Crea un dataframe `fifa20_best_shooting` que contenga a TODOS  los jugadores de los clubs encontrados en el ejercicio anterior.


## Pregunta 3

Calcula media y la desviación típica   del sueldo de cada equipo del dataframe `fifa20_best_shooting`. 



## Pregunta 4

Discretiza la variable `age` de  `fifa20_best_shooting` en los 3 niveles siguientes: “freshman”, “junior”, “senior”, según los cortes por defecto. La variable resultante age_Level tiene que ser un factor ordenado en orden creciente de edad. 


## Pregunta 5

¿Qué club tiene a más jugadores en el nivel "senior" calculado en el ejercicio anterior?



## Pregunta 6

¿Cuántas nacionalidades hay entre todos los jugadores de `fifa20_best_shooting`? ¿Qué club tiene mayor cantidad de nacionalidades?


## Pregunta 7

Calcula mediante un diagrama de barras ordenado de mayor a menor la proporción de jugadores de cada nacionalidad en cada club



## Pregunta 8

Encuentra la función (lineal, exponencial o potencial) que mejor describe la dependencia funcional del sueldo de los jugadores en función de la variable `shooting` en el dataframe `fifa20_best_shooting`. Representa dicha función junto con los puntos (shooting, sueldo) en escala lineal.
