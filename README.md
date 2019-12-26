# seq_tools-conda

This packs https://github.com/intbio/pytexshade into conda

## Building and uploading to Anaconda cloud
```
conda install -y conda-build
conda install -y anaconda-client
anaconda login

conda-build -c r -c conda-forge -c bioconda pytexshade 
anaconda upload --force path_to_package #or toggle automatic upload with: conda config --set anaconda_upload True
conda convert --platform all path_to_package -o output/
find output/ -name 'seq_tools*' -exec anaconda upload --force {} \;
#Manually upload for OSX and Linux
```

## Installing  from Anaconda cloud

```
conda install -c intbio pytexshade
```
