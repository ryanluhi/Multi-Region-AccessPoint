# Multi-Region-AccessPoint
Implement an **Amazon S3 Multi-Region Access Point (MRAP)** to provide low-latency, fault-tolerant access to objects stored in multiple AWS regions.

1. **Created S3 Buckets** in two different regions (`ap-southeast-2` and `ca-central-1`).
   ![create Bucket,enable bucket versioning,configure cross-region replication(CRR)](/mrap1.jpeg)

2. Enabled **Bucket Versioning** to support replication.
3. Configured **Cross-Region Replication (CRR)** between the buckets.
   ![create multi-region access point](/mrap3.jpeg)-
   ![Configured Cross-Region Replication(CRR) between the buckets.](/mrap4.jpeg)  
                                  
4. Created an **S3 Multi-Region Access Point** to unify access across regions.
![create multi-region access point](/mrap2.jpeg)-

5. Tested object uploads/downloads via the MRAP endpoint.
   
-create an object and uploaded it in the multi-region access point i created 'ap-southeast-2'
![create an object and insert it in the multi-region access point i created 'ap-southeast-2'](/mrap8.jpeg)

-uploaded in the 'ap-southeast-2' region bucket
![Testing](/mrap7.jpeg)

-after some few minutes it was replicated on the 'ca-central-1' region bucket
![testing](/mrap9.jpeg)

Key Learnings

-Multi-Region Access Point provides a single global endpoint for S3 access.
-Data is served from the nearest region, improving latency and resilience.
-Cross-Region Replication ensures data consistency across buckets.
-Useful for global applications requiring fast, reliable content delivery.

References

S3 Multi-Region Access Points(https://docs.aws.amazon.com/AmazonS3/latest/userguide/MultiRegionAccessPoints.html)


*Author: Ryan Luhongo
*Created on: August 2025
