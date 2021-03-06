# secret-yaml
Secret yaml values

## Goal

Lightweight tool to secret yaml values, 
which you can quickly install right inside your pipeline

## Install

```
export OS=$(uname | tr '[:upper:]' '[:lower:]')
curl -LsSo /usr/local/bin/syml https://github.com/antonmarin/secret-yaml/releases/latest/download/syml-${OS}
chmod +x /usr/local/bin/syml
```

## Usage

- `export SYML_SECRET=$(syml generateSecretKey)` 
generate secret and store inside env variable
- `syml encrypt --secret=${SYML_SECRET} 
~/decryptedSecrets/secret.yaml > ~/encryptedSecrets/secret.yaml`
encrypt values inside yaml-file and save to new file
- `syml decrypt --secret=${SYML_SECRET} 
~/encryptedSecrets/secret.yaml > ~/decryptedSecrets/secret.yaml`
decrypt values inside yaml-file and save to new file

`syml help` to get more about usage
