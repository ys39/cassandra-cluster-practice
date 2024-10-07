## Cassandra クラスタを構築するための docker-compose

- クラスタ数は 1、論理データセンターは 2 つ、ノード数は 3 で構築する。

  ```
  DC1
    - node1(rack1)
    - node2(rack2)
    - node3(rack3)
  DC2
    - node1(rack1)
    - node2(rack2)
    - node3(rack3)
  ```

1. docker-compose 起動

   ```bash
   docker-compose up -d
   ```

2. cqlsh に接続

   - cassandra の node に接続せずに、cqlsh コンテナを起動し、cqlsh に接続する。

   ```
   docker-compose run cqlsh
   ```
