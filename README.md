# Overview
Leverage these `YAML` templates to create the minimum needed components of a Splunk Cluster using the Splunk Operator on OpenShift 4.8.

Simply modify each template to have the desired `Namespace` to create these objects (subsitute "<namespace>")

## Templates
Each folder here contains a series of yaml templates that will create the following objects on OpenShift:
1. Splunk Operator CRD (indexer or search head)
2. Horizontal Pod Autoscaler (HPA)
3. OpenShift Route Definition

Deploying from each folder results in:
- 1x Splunk Indexer Cluster
- 1x Splunk Search Head Cluster
- 2x OpenShift Routes, 1 for each Splunk Service (https://<route-name>-<namespace>.<cluster>/)