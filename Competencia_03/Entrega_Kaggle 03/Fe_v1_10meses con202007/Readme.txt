1- Se crea la clase ternario con el C03_1_clase_ternaria.ipynb, el archivo de ingreso  = 'competencia_03_crudo.csv.gz', archivo de salida
' competencia_03.csv.gz'

2-se standariza por deflacion se guarda como  (competencia_03_corregido_deflacion.csv) 

3- Featur engineering:  %%sql
COPY competencia_03 TO '/home/ingceciliaconde/buckets/b1/datasets/03/competencia_03_fe_v1.csv.gz' (FORMAT CSV, HEADER TRUE);
 arranque con el archivo corregido por deflacion (competencia_03_corregido_deflacion.csv) , con ventana 3 

4 -Desde la maquina virtua se levana el archivo 'competencia_03_fe_v1.csv.gz', se utilizan los ultimos 10 meses

 Se optimiza optuna y se guarda en 
storage_name = "sqlite:///" + db_path + "optimization_lgbm_v9.db"
study_name = "exp_lgbm_v9_10meses_fe_v1"

corro con mis semillas originales mas 25 semillas al azar

