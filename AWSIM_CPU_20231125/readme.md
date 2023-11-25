# CPU実行環境(共通)
- AWSIM: 11/25現在
  - sha256sum: f36e0d3ec9c769d236862e035fee213abeea7d0e15c9743f7742a5041cddafbf
- aichallenge2023-racing: 11/25現在
  - commit: 71b3954158a2307ba3b684d9c88a6da34c09704e
- autoware-universe-no-cuda: 11/25現在
  - docker image id: b7fdf9678bc2
- 画面録画: Ubuntuの画面共有機能により、RDPクライアント側の画面を録画


# PCその1
- CPU: Intel Core i5-11500 6C12T(うち、VMwareで6Cを有効化)
- MEM: 32GB中16GBを割り当て
- SSD: 32GB
- OS: Ubuntu 22.04
- 仮想化: あり(VMWare ESXi 7.0)

# PCその2
- CPU: AMD Ryzen 7 7735HS 8C16T
- MEM: 32GB
- SSD: 1TB中64GBを割り当て
- OS: Ubuntu 22.04
- 仮想化: なし