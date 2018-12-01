
## Download file

```bash

SECRET_KEY=minio-artificerpi
ACCESS_KEY=minio-passw0rd
FILE_PATH=tmp/sample.png
DATE=$(date -R)
 
STRING_TO_SIGN="GET\n\n\n${DATE}\n/${FILE_PATH}"
SIGNATURE_VALUE=$(echo -en "${STRING_TO_SIGN}" | openssl sha1 -hmac "${ACCESS_KEY}" -binary | base64)
 
curl -X GET -T "" \
    -H "Authorization: AWS ${SECRET_KEY}:${SIGNATURE_VALUE}" \
    -H "Date: ${DATE}" \
    "http://${MINIO_HOST}:9000/${FILE_PATH}" \
    -O $(basename ${FILE_NAME})
``` 

## Reference
* https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html