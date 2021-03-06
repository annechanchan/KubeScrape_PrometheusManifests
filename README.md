<p align="center">
  <img src="https://i.imgur.com/763iZTq.jpg"  width="300" height="240">
</p>

## [KubeScrape](https://github.com/oslabs-beta/KubeScrape)
KubeScrape is an open-source dev tool that provides an intuitive way to view the health, structure, and live-metrics of your Kubernetes cluster.

Please visit the below github release repository to download the KubeScrape application with one-click and try our K8 visualizer for yourself! Our team would love to hear your feedback and suggestions for enhancements. Please leave a star to help support our work!

[KubeScrape](https://github.com/oslabs-beta/KubeScrape) | [![GitHub stars](https://img.shields.io/github/stars/oslabs-beta/KubeScrape?style=social&label=Star&)](https://github.com/oslabs-beta/KubeScrape/)

## KubeScrape_PrometheusManifests Overview
This repository contains manifest files to help KubeScrape users deploy an instance of Prometheus (including alert rules), node exporter, and kube-state-metrics into their Kubernetes cluster. Kubescrape will leverage these instances to gather metrics from the Kubernetes API and display them in the application. 

Please note the following ports being leveraged and update them as needed in the yaml files: 
  - Prometheus:
    - port: 9090 
    - targetPort: 9090
    - nodePort: 30000
  - Node Exporter: 
    - port: 9100 
    - targetPort: 9100
  - Kube-StateMetrics: 
    - ports: 8080, 8081
  
## Instructions 
To deploy the K8 objects in the "Manifest" files into your cluster, please follow the below 4 steps: 

1. (Optional Step) Fork this repository to your Github repositories
2. Clone the repo 
3. CD (Change directory) into the "KubeScrape_PrometheusManifest" folder
4. Run the following command in your terminal to create the "monitoring" namespace:  
  ```
  kubectl create namespace monitoring
  ```
5. Run the following command to create K8 objects for Prometheus, node exporter, and kube-state-metrics from the manifests folder:
  ```
  kubectl apply -f manifests
  ```
  
*Note: These K8 objects will persist in your cluster. If you would like to delete, navigate to this root folder and run: 
  ```
  kubectl delete -f manifests
  ```
