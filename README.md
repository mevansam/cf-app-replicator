# Cloud Foundry Application Replication Utility

## Overview

This application replicates applications and services between Cloud Foundry targets. 
It does this by listening to Firehose events that result in applications being created 
or modified and replicates these actions on the targets.

**Goals:**
- Copy an application deployed to the origin target to destination targets
- Synchronize application's environment across all targets
- Duplicate services applications are bound to by 
  1. Creating user-provided-services that point to service instances at oring
  2. Creating service instances at target that do not need to be synchronized

**Anti-Goals:**
- Replication of data services between targets

