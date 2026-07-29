## Networking on Google Cloud Platform (GCP)

### 1. Official documentation and resources at [Google Cloud docs](https://docs.cloud.google.com/docs/networking)
### 2. Key Terms and Concepts
- **Region**:
  - An independent geographic area where resources run
  - APAC (Asia and Australia), Europe, Africa, Middle East, North America, and South America
- **Virtual Private Cloud (VPC) network**
  - A virtualized network within Google Cloud
  - One of *global resources (\*)* and not associated with any particular region or zone
  - New projects start with a default network, an auto mode VPC network, that has one subnet in each region
  - Best practice is to create a custom mode VPC network and include subnets only in desired regions
- **Subnet**
  - One of *regional resources (\*)*
- **Global resources** - [details](https://docs.cloud.google.com/compute/docs/regions-zones/global-regional-zonal-resources#)
  - Global resources are accessible by any resource in any zone within the same project.
    When creating a global resource, there is no need to provide a scope specification
  - 
