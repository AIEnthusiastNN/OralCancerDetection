# Oral Lesion Screening App

Classes: Normal / Variation from Normal / OPMD / Oral Cancer

## Setup
1. Copy your trained weights into `backend/weights/`:
   resnet50.pth, convnext_tiny.pth, vit_tiny.pth, swin_tiny.pth, coatnet_0.pth
2. Run:

       docker compose up --build

- App: http://localhost:8080
- API docs: http://localhost:8000/docs

## Notes
- Weights are mounted as a volume (not baked into the image).
- Models load lazily on first request, so the first prediction is slower.
- If loading fails with key mismatches, set STRICT_LOAD=0 in docker-compose.yml.
- GPU: swap the torch install in backend/Dockerfile for CUDA wheels and run with the NVIDIA runtime.

## Run on a real phone (Expo Go)
    cd frontend && npm install
    EXPO_PUBLIC_API_URL=http://<YOUR-PC-IP>:8000 npx expo start
"# OralCancerDetection" 
"# OralCancerDetection" 
