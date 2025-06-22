# notebook-per-user Helm Chart

A Helm chart to manage per-user permissions for OpenShift AI workbenches (notebooks).

## Overview

This chart provides a workaround for managing notebook permissions on a per-user basis in OpenShift AI environments.

## Usage

1. **Set Naming Conventions:**  
   Decide on a naming convention for user notebooks (e.g., `${username}-nb`).

2. **Configure Cluster Role:**  
   Edit `templates/user-notebook-cluster-role.yaml` and update the `resourceNames` field to match your chosen naming convention.

3. **Update Values:**  
   Edit `values.yaml` to specify the desired user names and namespaces.

4. **Install the Chart:**  
   ```sh
   helm install notebook-per-user . -f values.yaml
   ```
