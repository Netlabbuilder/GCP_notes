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
- **Zones**
  - GCP Regions are divided into zones
- **Virtual Private Cloud (VPC) networks**
  - A VPC network is a virtualized network within Google Cloud
  - One of *global resources (\*)* and not associated with any particular region or zone
  - New projects start with a default network, an auto mode VPC network, that has one subnet in each region
  - Best practice is to create a custom mode VPC network and include subnets only in desired regions
- **Subnets**
  - One of *regional resources (\*\*)*
- **Global resources** - [more details can be found here](https://docs.cloud.google.com/compute/docs/regions-zones/global-regional-zonal-resources#)
  - Global resources are accessible by any resource in any zone within the same project.
    When creating a global resource, there is no need to provide a scope specification
  - 
