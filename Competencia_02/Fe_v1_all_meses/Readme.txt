1- Se crea la clase ternario con el C02_1_clase_ternaria.ipynb, el archivo de ingreso  = 'competencia_02_crudo.csv.gz', archivo de salida
' competencia_02.csv.gz'

2-c02_2_preprocesoamiento: se standariza por deflacion se guarda como  (competencia_02_corregido_deflacion.csv) 

3-C02_4_Featur engineering_en SQL: 
A partir del archivo del punto 2 se corre el scrip para finalmente ser guardao el archivo como 'competencia_02_fe_v1.csv.gz'
 
4 -C02_7_Lgb_avanzado: 
Se levana el archivo 'competencia_02_fe_v1.csv.gz', se utilizan todo los  meses par entrenarde entrenamiento

Se optimiza optuna y se guarda en 
storage_name = "sqlite:///" + db_path + "optimization_lgbm_v6.db"
study_name = "exp_lgbm_v6_allmeses_fe_v1"

El scrip envia a kaggle el archivo de cada semila con dada corte y luego calcula el promedio de cada de las probabilidades de cada uno de los modelos.

  nombre_archivo = f"C2_CC_30_fev1_ensamblepromedio{num_subida_kaggle}.csv"

  Elegi el que mas ganancia de mio.
