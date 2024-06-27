# **IQTREE**
Debe crear una carpeta Iqtree y descargar iqtree2 para Windows comprimido zip
wget https://github.com/iqtree/iqtree2/releases/download/v2.2.0/iqtree-2.2.0-Windows.zip

Descomprimir el archivo zip
unzip iqtree-2.2.0-Windows.zip

Trasladar el archivo IQ-TREE al directorio de ejecutables:
Mover el archivo descomprimido a un directorio que esté en tu PATH.
Ejemplo: puedes moverlo a C:\Program Files\Iqtree y luego agregar esta ruta al PATH.
Pasos para agregar la ruta al PATH en Windows:
a. Copiar la ruta donde se decomprimió IQ-TREE. Ejemplo: C:\Program Files\Iqtree
b. Abrir el panel de control e ir a Sistema y seguridad -> Sistema -> Configuración avanzada del sistema.
c. Hacer clic en Variables de entorno.
d. En la sección Variables del sistema, buscar la variable Path y selecciona Editar.
e. Realizar clic nuevamente Nuevo e ingresar la ruta a la carpeta donde se descomprimió IQ-TREE.Ejemplo, C:\Program Files\Iqtree\bin
f. Hacer clic en Aceptar en todas las ventanas abiertas para aplicar los cambios.
Verificar la instalación:
Abre Git Bash y escribe el siguiente comando para verificar que IQ-TREE se ha instalado correctamente y está en tu PATH:

```
iqtree2 -h
```

Este comando debería mostrarte la ayuda de IQ-TREE, confirmando que la instalación ha sido exitosa.


# **Genes ortólogos**

## 1. Descargar genes ortólogos de mamíferos 
Ir a la página de NCBI y descargar las secuencias de placentals, rodents, beavers and others y mice and others en formato Fasta.

```
https://www.ncbi.nlm.nih.gov/gene/7157/ortholog/?scope=7776,1963757,1963758&term=TP53
```

# **Alineación**

## 1. Abrir el programa Muscle en línea

```
https://www.ebi.ac.uk/jdispatcher/msa/muscle/summary?jobId=muscle-I20240624-214541-0023-97659465-p1m&js=pass
```

![Programa](https://kbase.us/services/narrative_method_store/img?method_id=kb_muscle/MUSCLE_nuc&image_name=muscle-cyan.png)

## 2. Subir archivo Fasta "Trp53_refseq_transcript.fasta" al programa Muscle en línea y correr.


## 3. Se genera un archivo alineado en formato Fasta
 ```
alineamiento.aln-fasta
```

# **Análisis filogenético**

## 1. Correr Iqtree2 con el archivo alineado

```
iqtree2 -s alineamiento.aln-fasta -B 1000
```

## 2. Generar varios archivos y escoger entre ellos, "alineamiento.aln-fasta.treefile".

```
alineamiento.aln-fasta.treefile
```

Abrir el archivo "alineamiento.aln-fasta.treefile" con el programa FigTree. 


