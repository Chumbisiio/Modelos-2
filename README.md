# Predicción del tabaquismo y del consumo de alcohol

Proyecto de Modelos y Simulación de Sistemas II, Universidad de Antioquia. Comparamos cinco familias de modelos con datos de chequeos de salud. El tabaquismo se clasifica en tres estados y el consumo de alcohol en sí o no.


## Ejecutar en Google Colab

1. Abre el notebook Smoking_and_Drinking_Dataset_with_body_signal_Grupo_3.ipynb en una sesión nueva de Colab y ejecuta las celdas de arriba abajo. La **fase 0** instala las dependencias y descarga el CSV completo desde el enlace público del proyecto.
2. Después de la limpieza, verifica que queden **991.005 filas y 24 variables de entrada**. La partición debe mostrar **792.804 filas de entrenamiento y 198.201 de prueba**.
3. La fase 6 genera `mejores_hiperparametros.json`. La búsqueda tomó unos 91 minutos en la corrida registrada. La fase 9 genera un CSV con **10 filas**, una por modelo y tarea.
4. Descarga los resultados del panel de archivos de Colab antes de cerrar la sesión. El espacio de trabajo `/content` es temporal.

## Retomar con los hiperparámetros guardados

Sube `mejores_hiperparametros.json` a `/content`. Ejecuta las fases **0 a 3**, la celda **4.1** y las celdas de **6.1**. Salta los cinco bloques de búsqueda de **6.2** y ejecuta **Preparar hiperparámetros para las fases siguientes**. Deben aparecer 10 pares de modelo y tarea. Desde ahí puedes seguir con las fases **7 a 9**, o pasar directamente a la **fase 9** para repetir solo la prueba final.

## Resultados

Todos los archivos se generan en `/content`.

| Fases | Archivos principales |
| --- | --- |
| 4–5 | `resultados_seccion4.csv`, `resultados_seccion4_5.csv` |
| 6–7 | `mejores_hiperparametros.json`, `resultados_grupos.csv`, `grupos_variables.png` |
| 8 | `analisis_individual.csv`, `resultados_reduccion.json`, `resultados_reduccion_pca.json`, `resultados_sin_candidatas.json`, `resultados_umap.json` |
| 9 | `resultados_final_prueba.csv` |

Para consultar las cifras sin recalcular, usa las salidas guardadas en el notebook o los CSV y JSON del proyecto. La ejecución registrada usó Python 3.13, scikit-learn 1.6.1 e iterative-stratification 0.1.9. Las versiones y el equipo pueden afectar tiempos y métricas.
