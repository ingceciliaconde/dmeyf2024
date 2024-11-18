1- Se crea la clase ternario con el C02_1_clase_ternaria.ipynb, el archivo de ingreso  = 'competencia_02_crudo.csv.gz', archivo de salida
' competencia_02.csv.gz'

2-Desde la maquina virtua se levana el archivo 'competencia_02.csv.gz', se utilizan 12 meses de entrenamiento

3- Se optimiza optuna y se guarda en 
storage_name = "sqlite:///" + db_path + "optimization_lgbm_v1.db"
study_name = "exp_lgbm_v1_12meses"

termine el scrip c02_7_lgb_avanzado en donde armo los modelos con mis 5 semillas y luego hago entregas con varios cortes 
y al final hago un ensamble de probabilidad promedio .

a los modelos los llame: f'lgb_v5_semilla{semilla}_{cantidad_meses_train}_{ventana

ojo aca tuve que acomodar los index.

los modelos por separado daban algo asi en promedio de menos de 100 y juntos el mayor llega a 112.
