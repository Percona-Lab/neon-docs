graph TD
    A[Compute node] -->|Page IO| B([pageserver])
    A[Compute node] -->|WAL write| C([WAL safekeeper])
    C --> B
    B --> |durable writes| D[[S3 Object Storage]]
