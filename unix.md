## Compression

### Tar'ing a file
```
tar -cvf <tar_file_name.tar> <folder to tar>
```

### Un-Tar'ing a file
```
tar -xvf <tar_file_name.tar> <folder to tar>
```

### How to unzip a file
```
unzip filename.zip
```



### SCP'ing a file onto a machine
```
scp -i <location_of_pem_file> <file_to_transfer> user@machineip:/<location_to_upload_to>
```

### SCP'ing a file from a machine
```
scp -i <location_of_pem_file> user@machineip:<file_to_transfer> <folder_to_transfer_to>
```

### SSH'ing into a machine with a pem file
```
ssh -i <location_of_pem_file> user@machineip
```
