---
title: "Horizontal Pod Autoscaler"
sidebar_position: 10
sidebar_custom_props: { "module": true }
description: "Automatically scale workloads on Amazon Elastic Kubernetes Service with Horizontal Pod Autoscaler."
---

::required-time

In this lab, we'll look at the Horizontal Pod Autoscaler (HPA) to scale pods in a deployment or replica set. It's implemented as a K8s API resource and a controller. The resource determines the behavior of the controller. The Controller Manager queries the resource utilization against the metrics specified in each HorizontalPodAutoscaler definition. The controller periodically adjusts the number of replicas in a replication controller or deployment to the target specified by the user by observing metrics such as average CPU utilization, average memory utilization or any other custom metric. It obtains the metrics from either the resource metrics API (for per-pod resource metrics), or the custom metrics API (for all other metrics).

The Kubernetes Metrics Server is a scalable and efficient aggregator of resource usage data in your cluster. It provides container metrics that are required by the Horizontal Pod Autoscaler. The metrics server is not deployed by default in Amazon EKS clusters.

<img src={require('./assets/hpa.webp').default}/>
