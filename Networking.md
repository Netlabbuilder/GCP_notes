## Networking on Google Cloud Platform (GCP)

### 1. Official documentation and resources at [Google Cloud docs](https://docs.cloud.google.com/docs/networking)
### 2. Key Terms and Concepts
- **Regions**
  - A GCP region is an independent geographic area where resources run
  - Regions:
    - APAC - Asia `asia` and Australia `australia`
    - Europe `europe`
    - Africa `africa`
    - Middle East `me`
    - North America - US `us`, Canada and Mexico `northamerica`
    - South America `southamerica`
  - Each GCP has zones, typically at least three zones
  - Resource distribution:
    - Resources into regions and zones:
      - Redundancy in case of failure
      - Latency improvement by locating resources closer to clients
- **Zones**
  - GCP Regions are divided into zones - `a`, `b`, `c`...
  - A single failure domain within a region
  - Resource distribution:
    - Resources into regions and zones:
      - Redundancy in case of failure
      - Latency improvement by locating resources closer to clients
  - There are specialized zones for AI and ML workloads:
    - GPU locations - [more details can be found here](https://docs.cloud.google.com/compute/docs/regions-zones/gpu-regions-zones)
    - TPU locations - [more details can be found here](https://docs.cloud.google.com/compute/docs/regions-zones/tpu-regions-zones)
    - AI Zones - [more details can be found here](https://docs.cloud.google.com/compute/docs/regions-zones/ai-zones)
- **Virtual Private Cloud (VPC) networks**
  - A VPC network is a virtualized network within Google Cloud
  - One of *global resources (\*)* and not associated with any particular region or zone
  - New projects start with a default network, an auto mode VPC network, that has one subnet in each region
  - Best practice is to create a custom mode VPC network and include subnets only in desired regions
- **Subnets**
  - One of *regional resources (\*\*)*
- **Global, regional, and zonal resources**
  - **Global resources** - [more details can be found here](https://docs.cloud.google.com/compute/docs/regions-zones/global-regional-zonal-resources#)
    - Global resources are accessible by any resource in any zone within the same project
    - No scope specification when creating a global resource
