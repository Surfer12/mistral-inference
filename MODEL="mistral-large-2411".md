MODEL="mistral-large-2411" '


url="https://${us-central1}-aiplatform.googleapis.com/v1/projects/${}/locations/${GOOGLE_REGION}/publishers/mistralai/models/${MODEL}:rawPredict"

curl \
  -X POST \
  -H "Authorization: Bearer $(gcloud auth print-access-token)" \
  -H "Content-Type: application/json" \
  $url \
  --data '{
    "model": "'"$MODEL"'",
    "temperature": 0,
    "messages": [
      {"role": "user", "content": "What is the best French cheese?"}
    ]
}'

//ryanoatsie@cloudshell:~()$ MODEL="mistral-large-2411"


url="https://$GOOGLE_REGION-aiplatform.googleapis.com/v1/projects/$((/locations/$GOOGLE_REGION/publishers/mistralai/models/$MODEL:rawPredict"


curl \
  -X POST \
  -H "Authorization: Bearer $(gcloud auth print-access-token)" \
  -H "Content-Type: application/json" \
  $url \
  --data '{
    "model": "'"$MODEL"'",
}'  ] {"role": "user", "content": "What is the best French cheese?"}
curl: (6) Could not resolve host: -aiplatform.googleapis.com

