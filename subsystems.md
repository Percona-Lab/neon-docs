```
graph TD
    A[Compute node] -->|Page IO| B[(pageserver)]
    A[Compute node] -->|WAL write| C([WAL safekeeper])
    C --> B
    subgraph pageserver system
    B --> |durable writes| D[[S3 Object Storage]]
    end
```


![diagram](https://mermaid.ink/img/pako:eNp1UctOwzAQ_BVrT1RKqxIndeIDUh8ckEBFKhISSQ5uvW1DGyeyHaA0_XecBJUTPu3OzM6OtWfYlBKBw06Lak9eFqki7k2TeVlUtUWiHJ2R4fCueRY7JA_LhsySm8rVBvUH6kH2_8Tr9JF86txiQ-Y3SdsZscUDYoU6G_Rz81ZJZn1j6nWf48-fmJOxWPT8rBM3stZifcTe2zRkkSQrSpbrd9xYsrKldtPZby5UMlWpAg8K1IXIpfvruaVSsHssMAXuSin0IYVUXZxO1LZcndQGuNU1elBXUlhc5MJFK4BvxdFc0XuZu3VXsBIK-Bm-gNMJG41jSn0WRywMGPPgBDymI3YbBn40prSFLx58l6UzHY9YFPh-PPHDIGSMRR5gZ_3UX6c7Uuf_1um7fZcfZ5eL4A?type=png)
