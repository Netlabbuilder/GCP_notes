- VPC Peering verification:

  -
  `gcloud compute networks peerings list --network=vpc-3`

  - 
  ```
    $ gcloud compute networks peerings list --network=vpc-3
    NAME: peering-vpc3-vpc2
    NETWORK: vpc-3
    PEER_PROJECT: learning-cloud-460908
    PEER_NETWORK: vpc-2
    STACK_TYPE: IPV4_ONLY
    PEER_MTU: 8896
    IMPORT_CUSTOM_ROUTES: True
    EXPORT_CUSTOM_ROUTES: True
    UPDATE_STRATEGY: INDEPENDENT
    STATE: ACTIVE
    STATE_DETAILS: [2026-10-11T06:33:34.789-07:00]: Connected.
    $ gcloud compute networks peerings list-routes peering-vpc3-vpc2  --network=vpc-3 --region=us-west1  --direction=INCOMING
    DEST_RANGE: 10.2.1.0/24
    TYPE: SUBNET_PEERING_ROUTE
    NEXT_HOP_REGION: us-west1
    PRIORITY: 0
    STATUS: accepted
    $ gcloud compute networks peerings list-routes peering-vpc3-vpc2  --network=vpc-3 --region=us-west1  --direction=OUTGOING
    DEST_RANGE: 10.3.1.0/24
    TYPE: SUBNET_PEERING_ROUTE
    NEXT_HOP_REGION: asia-southeast1
    PRIORITY: 0
    STATUS: accepted by peer
    $ 
  ```
