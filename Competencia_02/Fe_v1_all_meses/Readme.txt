1- Se crea la clase ternario con el C02_1_clase_ternaria.ipynb, el archivo de ingreso  = 'competencia_02_crudo.csv.gz', archivo de salida
' competencia_02.csv.gz'

2-se standariza por deflacion se guarda como  (competencia_02_corregido_deflacion.csv) 

3- Featur engineering:  %%sql
COPY competencia_02 TO '/home/ingceciliaconde/buckets/b1/datasets/competencia_02_fe_v1.csv.gz' (FORMAT CSV, HEADER TRUE);
 arranque con el archivo corregido por deflacion (competencia_02_corregido_deflacion.csv) , con ventana 3 

4 -Desde la maquina virtua se levana el archivo 'competencia_02_fe_v1.csv.gz', se utilizan todo los  meses de entrenamiento

 Se optimiza optuna y se guarda en 
storage_name = "sqlite:///" + db_path + "optimization_lgbm_v6.db"
study_name = "exp_lgbm_v6_allmeses_fe_v1"

termine el scrip c02_7_lgb_avanzado en donde armo los modelos con mis 5 semillas y luego hago entregas con varios cortes 
y al final hago un ensamble de probabilidad promedio .

a los modelos los llame: f'lgb_v5_semilla{semilla}_{cantidad_meses_train}_{ventana


