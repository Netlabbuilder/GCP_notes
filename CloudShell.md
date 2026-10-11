- VPC Peering:

  - To list all VPC peerings within a VPC, please use `gcloud compute networks peerings list --network=VPC_NAME` (replace `VPC_NAME` with a valid VPC name):
    
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
    $
    ```
  - To list all routes received from and advertised to peered VPC:
    - To list all routes received from peered VPC, please use `--direction=INCOMING`:    
      ```
      $ gcloud compute networks peerings list-routes peering-vpc3-vpc2  --network=vpc-3 --region=us-west1  --direction=INCOMING
      DEST_RANGE: 10.2.1.0/24
      TYPE: SUBNET_PEERING_ROUTE
      NEXT_HOP_REGION: us-west1
      PRIORITY: 0
      STATUS: accepted
      $
      ```
    - To list all routes advertised to peered VPC, please use `--direction=OUTGOING`:
      ```
      $ gcloud compute networks peerings list-routes peering-vpc3-vpc2  --network=vpc-3 --region=us-west1  --direction=OUTGOING
      DEST_RANGE: 10.3.1.0/24
      TYPE: SUBNET_PEERING_ROUTE
      NEXT_HOP_REGION: asia-southeast1
      PRIORITY: 0
      STATUS: accepted by peer
      $ 
      ```
