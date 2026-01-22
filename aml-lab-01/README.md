# AML Lab 01 — Pierwszy eksperyment (CLI v2)

## Uruchomienie
az extension add -n ml -y
az configure --defaults group=rg-aml-49532 workspace=amlws-49532 location=francecentral
az ml compute create --name cpu-cluster-49532 --type amlcompute --size Standard_DS2_v2 --min-instances 0 --max-instances 1 --idle-time-before-scale-down 120
az ml job create --file job.yml --stream

## Wyniki
- Metryki: accuracy (Azure ML Studio → Experiments → intro-sklearn)
- Artefakty:
  - outputs/model.joblib
  - outputs/metrics.json
