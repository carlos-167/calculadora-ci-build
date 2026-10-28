# Calculadora CI

Practica de CI/CD con GitHub Actions.

Es una calculadora sencilla en Python (suma, resta, multiplicacion y division) con una prueba en pytest. Cada vez que hago push se ejecuta el pipeline.

## Correr las pruebas

```
pip install pytest
python -m pytest
```

## Pipeline

El workflow esta en `.github/workflows/ci.yml` y hace esto:

1. Instala pytest
2. Ejecuta las pruebas
3. Build: copia `calculadora.py` a la carpeta `artefactos`
4. Comprime la carpeta en `artefacto.zip`
5. Sube el zip como artefacto (`build-python`)

El artefacto se descarga desde la pestaña Actions, entrando a la ejecucion.
