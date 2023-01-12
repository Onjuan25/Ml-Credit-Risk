Estudio sobre análisis particular de riesgo crediticio, con su correspondiente modelo de predicción.

Para el caso de estudio se utiliza el dataset de riesgo de crédito provisto por la página https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction descargando y trabajandolo localmente, aunque se tiene en consideración la escalabilidad del proyecto, por lo que se utilizarán librerías de estadìstica y modelado de datos.

Particularmente, el análisis a los datos preeliminares se realizará con un método llamado 'vintage analysis' el cual para el caso de riesgo crediticio crea una segmentación por períodos de tiempo para los deudores, separando deudores morosos del resto. Éste análisis ayudará a la comprensión del tema a tratar.

Cabe destacar que el proyecto apunta a considerar factores de riesgo facilmente reconocible y en ningún momento se atenderá a realizar un análisis mas profundo de riesgo sistémico, algo para lo cual un simple modelo no pretende abarcar.

Una vez realizado el análisis preeliminar de los datos, para conocer un poco mas del portfolio al que referencia el dataset, tenemos una idea clara sobre cómo utilizar los datos para una mejor predicción y para no afectar futuras aplicaciones pero tampoco otorgar créditos a demasiados clientes potencialmente morosos o incapaces de cumplir con la obligación crediticia.

Luego queda resolver un gran problema presente en éste analisis como también en otros dedicados a detectar anomalías, lo difícil es que suelen representar una porcion muy pequeña del dataset, por lo que hay que recurrir a técnicas de modelado para 'balancear' los datos y que tanto crédito bueno como crédito malo(clase minoritaria) tengan la misma proporción, si no sucede ésto luego en el segmento de predicción puede que el modelo comunmente haga 'overfitting', lo que se traduce en que no sirva para predecir y no funcione en futuras pruebas en un ambiente menos controlado.

La resolución se da usando el métodos de SMOTE(Synthetic Minority Over-sampling Technique) con el cual mejoramos el score de todos los modelos que se probaron, aunque se termina eligiendo al clasificador de arboles de decisión, sobre el cual se trabajaran los hyperparámetros correspondientes para mejorar la performance.
