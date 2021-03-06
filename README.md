# Alkaid

[![Github Action](https://github.com/yakumioto/alkaid/workflows/alkaid/badge.svg)](https://github.com/yakumioto/alkaid/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/yakumioto/alkaid)](https://goreportcard.com/report/github.com/yakumioto/alkaid)
[![codecov](https://codecov.io/gh/yakumioto/alkaid/branch/master/graph/badge.svg)](https://codecov.io/gh/yakumioto/alkaid)

[中文文档](README-zh.md)

Alikid is a BaaS (Blockchan as a Service) service based on Hyperledger Fabric

Currently in the design stage, plans to support docker, docker swarm, kubernetes

Alikid's predecessor was [hlf-deploy](https://github.com/yakumioto/alkaid/tree/v0.2.0) for rapid deployment and adjustment of Hyperledger Fabric networks

```text
+-------------------------------------------------------------+
|                                                             |
|                      BaaS Frontend                          |
|                                                             |
+-----+-------------------------------------------------+-----+
      |                                                 |
      |                                                 |
      v                                                 v
+-----+-------------------------------------------------+-----+
|                                                             |
|                      BaaS Backend                           |
|                                                             |
+-----+-------------------------------------------------+-----+
      |                                                 |
      |                                                 |
      v                                                 v
+-----+-------------------------------------------------+-----+
|                                                             |
|                    Docker / K8S / K3S                       |
|                                                             |
+---------+-------------------+--------------------+----------+
          |                   |                    |
          |                   |                    |
          v                   v                    v
    +-----+-----+       +-----+-----+        +-----+-----+
    |           |       |           |        |           |
    |  Net 001  |       |  Net 002  |        |  Net 003  |
    |           |       |           |        |           |
    +-----+-----+       +-----+-----+        +-----+-----+
          |                   |                    |
          |                   |                    |
          v                   v                    v
 +--------+-------------------+--------------------+----------+
 |                                                            |
 |   Virtual or Physical Machine / Public or Private Cloud    |
 |                                                            |
 +------------------------------------------------------------+

```

## Community

Telegram: <https://t.me/fab_alkaid>

## hlf-deploy

Supported features:

- channel create
- channel updateAnchorPeer
- channel join
- channel update (Update BatchTimeout, BatchSize)
- chaincode install
- chaincode instantiate
- chaincode upgrade
- chaincode invoke
- chaincode query
- organization join (Add organization dynamically, supported system channel)
- organization delete (Delete organization dynamically, supported system channel)
- organization update (Dynamically modify organization certificate, supported system channel)
- channel consensus (Switch consensus algorithm, supported solo, kafka, etcdraft)