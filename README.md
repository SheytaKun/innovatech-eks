\# Innovatech EKS



Repositorio unificado para el despliegue de Innovatech en Amazon EKS.



\## Estructura



\- `frontend/`: aplicación web frontend.

\- `backend/`: servicios backend de Ventas y Despachos.

\- `k8s/`: manifests Kubernetes.

\- `.github/workflows/`: pipeline CI/CD con GitHub Actions.



\## Arquitectura



La aplicación se despliega en Amazon EKS utilizando imágenes almacenadas en Amazon ECR.



Componentes principales:



\- Frontend expuesto mediante LoadBalancer.

\- Backend Ventas como servicio interno ClusterIP.

\- Backend Despachos como servicio interno ClusterIP.

\- Base de datos MySQL como servicio interno ClusterIP.

\- Autoscaling mediante Horizontal Pod Autoscaler.



\## Despliegue manual



Conectar kubectl al clúster:



```bash

aws eks update-kubeconfig --region us-east-1 --name EKS-Innovatech

