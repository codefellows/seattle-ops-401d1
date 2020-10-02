# Ops Challenge - Signature-based Malware Detection Part 3 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```bash

curl -v --request POST \
  --url 'https://www.virustotal.com/vtapi/v2/file/report' \
  -d apikey=$your-api-key \
  -d 'resource=$your-file-hash'
  

```
