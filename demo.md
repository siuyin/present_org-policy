Run up a OPA server:
```
opa run --server \
--log-format text \
--set decision_logs.console=true \
--set bundles.play.polling.long_polling_timeout_seconds=45 \
--set services.play.url=https://play.openpolicyagent.org \
--set bundles.play.resource=bundles/Bu0m4i9SFR
```

Execute queries against that server:
```
curl localhost:8181/v1/data -d '{"input":{"country":"Wakanda","dob":"2020-01-01T00:00:00Z"}}'
curl localhost:8181/v1/data -d '{"input":{"country":"Wakanda","dob":"2000-01-01T00:00:00Z"}}'
curl localhost:8181/v1/data -d '{"input":{"country":"Zingge","dob":"2000-01-01T00:00:00Z"}}'

curl localhost:8181/v1/data -d '{"input":{"country":"badCountry","dob":"2000-01-01T00:00:00Z"}}'
```
