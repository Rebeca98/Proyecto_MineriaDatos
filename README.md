# Proyecto_MineriaDatos

1. Clonar el entorno de conda con `conda env create nombre`.

2. Comando para sacar presentación

`cd propuesta`

```
pandoc -t revealjs -V theme=moon --mathjax --slide-level=2 -s Propuesta.md -o prop.html
```

3. Para activar el entorno: ` conda activate nombreEnv`
4. Para ver qué entornos tienes: `conda env list` o `conda info --envs`


### Paquetes para instalar:
`conda install jupyter notebook`
`conda install -c conda-forge tensorflow`
`conda install -c conda-forge matplotlib`
`conda install -c anaconda pandas`
`conda install -c anaconda numpy`
`conda install -c jmcmurrayy os`

# check installed packages in conda env 
`conda list`
