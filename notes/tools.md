Azure Tools for Infrastructure Management and Landing Zones

This document outlines tools I’ve explored for managing Azure infrastructure and deploying landing zones, including both Microsoft-native and open-source solutions.


1. Azure CLI

Command-line interface for managing Azure resources via terminal.


Examples:
```bash
az login
az group create --name myRG --location eastus
az vm create --resource-group myRG --name myVM --image UbuntuLTS

