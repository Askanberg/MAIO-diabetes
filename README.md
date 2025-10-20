# Virtual-Diabetes-Clinic-Triage-

# Diabetes Risk Service

This project is a small ML-service designed to predict shortterm diabetes progression by using the open *scikit-learn Diabetes* dataset. 
The Project i build to reproduce **MLOps-pipeline** with **GitHub Actions** and **Docker**

---

## Command to run the project

Build Docker-image
```bash
docker pull ghcr.io/askanberg/maio-diabetes:v0.1
```
Run containern
```bash
docker run -p 8000:8000 ghcr.io/askanberg/maio-diabetes:v0.1
```
To try the other one print v0.2 instead
Open in browser:
```bash
http://localhost:8000/health
```
Excepted answer:
```bash
{"status": "ok", "model_version": "0.1.0"}
```
Example payload using /predict
send with curl:
```bash
curl -Method POST http://localhost:8000/predict `
-Headers @{ "Content-Type" = "application/json" } `
-Body '{
  "age": 0.02,
  "sex": -0.044,
  "bmi": 0.06,
  "bp": -0.03,
  "s1": -0.02,
  "s2": 0.03,
  "s3": -0.02,
  "s4": 0.02,
  "s5": 0.02,
  "s6": -0.001
}'
```
Expected answer:
```bash
{"prediction": 235.9}
```

#License
Assignment 3 in MAIO course

#Contrubuting
Every team member of the group did great! Alexander Sätre, Andreas Skånberg, Samuel Laden, Melissa Westberg




