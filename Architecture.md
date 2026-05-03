# Architecture Overview

## Flow

Push event -> Initiation -> Dockerhub/AWS configuration -> Buildx setup -> Image build -> Image Pushed -> Export image_uri -> Pull image -> Add server host -> ssh action and blue green deployment

---

## Key Components

1. Workflow dispatch
2. Environment Variables
3. Configuration
4. Building, pushing, exporting
5. SSH to server
6. multiple smoke tests
