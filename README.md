# KubeScrape 
KubeScrape is XXX. High level overview about the project. 

Please visit the below github repository to download the KubeScrape application and try our K8 visualizer for yourself! Our team would love to hear your feedback and suggestions for enhancements. 
  Link: https://github.com/oslabs-beta/KubeScrape

## KubeScrape_PrometheusManifests Overview
The repository contains manifest files to help KubeScrape users deploy Prometheus, Node Exporter, and Kube-State-Metrics if Prometheus is not already deployed in their Kubernetes cluster. These configurations will help scrape metrics from the Kubernetes API. 

Please note the following ports being leveragedand update them as needed in the yaml files: 
  Prometheus:
    port: 9090 
    targetPort: 9090
    nodePort: 30000
  Node Exporter: 
    port: 9100 
    targetPort: 9100
  Kube-StateMetrics: 
    ports: 8080, 8081
  
##Instructions 
To deploy the K8 objects in the "Manifest" files into your cluster, please follow the below easy 3-4 steps: 

(Optional Step) Fork this repository to your Github repositories. (This will allow you to save any file updates to your repo). 
1. Clone the repo 
2. CD (Change directory) into the "KubeScrape_PrometheusManifest" folder
3. Run the following command in your terminal: 
  - ````kubectl apply -f Manifests```` 
