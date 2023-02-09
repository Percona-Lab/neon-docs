<code>
graph TD
    A[Compute node] -->|Page IO| B([pageserver])
    A[Compute node] -->|WAL write| C([WAL safekeeper])
    C --> B
    B --> |durable writes| D[[S3 Object Storage]]
</code>

![alt text](https://mermaid.ink/img/pako:eNp1UMFuwjAM_RXLJybBabcekGi7wyQQSJ20Q9KDaQwUSBqlyRAi_PvSVmKn-fTes5-f7Ac2nWLM8OjInuCrlAZSrUTRaRs8g0ntGhaLZdzRkeFzGyGfCZtwz-6HXf32v-N7tYabaz1HKGZiYD0d-MJs_3zFMAn5RPKRRBUc7a88efsIpRDVO2z3Z248VL5zKb2upZEG56jZaWpVOuExLJHoT6xZYpagIneRKM0zzVHwXXU3DWbeBZ5jsIo8ly2lyzVmB7r2L_VDtSnlJfJIN9Ojxn89fwE_eWZV?type=png)

