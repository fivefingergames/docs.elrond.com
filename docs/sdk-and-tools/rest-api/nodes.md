---
id: nodes
title: Nodes
---

Query Nodes (Peers) information.

## <span class="badge badge-primary">GET</span> **Get Heartbeat Status**

`https://gateway.elrond.com/node/heartbeatstatus`

This endpoint allows one to query the status of the Nodes.

<!--DOCUSAURUS_CODE_TABS-->

<!--Request-->

<!--Response-->

🟢 200: OK

Heartbeat status is retrieved successfully.

```
{
  "heartbeats": [
    ...
    {
      "timeStamp": "2020-06-04T16:02:41.191947208Z",
      "publicKey": "006d...",
      "versionNumber": "v1.0.125-0-g2164f5f04/go1.13.4/linux-amd64",
      "nodeDisplayName": "DrDelphi4",
      "identity": "stakingagency",
      "totalUpTimeSec": 7367,
      "totalDownTimeSec": 0,
      "maxInactiveTime": "1m41.148001375s",
      "receivedShardID": 4294967295,
      "computedShardID": 4294967295,
      "peerType": "eligible",
      "isActive": true
    },
    {
      "timeStamp": "2020-06-04T16:02:29.567740999Z",
      "publicKey": "667a...",
      "versionNumber": "v1.0.125-0-g2164f5f04/go1.13.4/linux-amd64",
      "nodeDisplayName": "DrDelphi0",
      "identity": "stakingagency",
      "totalUpTimeSec": 7367,
      "totalDownTimeSec": 0,
      "maxInactiveTime": "1m9.537847751s",
      "receivedShardID": 4294967295,
      "computedShardID": 4294967295,
      "peerType": "eligible",
      "isActive": true
    },
    ...
  ]
}
```

<!--END_DOCUSAURUS_CODE_TABS-->

## <span class="badge badge-primary">GET</span> **Get Statistics**

`http://localhost:8080/node/statistics`

This endpoint allows one to query statistics of the Node.

<!--DOCUSAURUS_CODE_TABS-->

<!--Request-->

<!--Response-->

🟢 200: OK

Statistics retrieved successfully.

```
{
  "statistics": {
    "liveTPS": 0,
    "peakTPS": 0,
    "blockNumber": 0,
    "roundNumber": 0,
    "roundTime": 5,
    "averageBlockTxCount": 0,
    "totalProcessedTxCount": 0,
    "shardStatistics": [
      {
        "liveTPS": 0,
        "averageTPS": null,
        "peakTPS": 0,
        "currentBlockNonce": 0,
        "totalProcessedTxCount": 0,
        "shardID": 0,
        "averageBlockTxCount": 0,
        "lastBlockTxCount": 0
      },
      {
        "liveTPS": 0,
        "averageTPS": null,
        "peakTPS": 0,
        "currentBlockNonce": 0,
        "totalProcessedTxCount": 0,
        "shardID": 0,
        "averageBlockTxCount": 0,
        "lastBlockTxCount": 0
      }
    ],
    "lastBlockTxCount": 0,
    "nrOfShards": 2
  }
}
```

<!--END_DOCUSAURUS_CODE_TABS-->

:::important
This endpoint is not available on the Proxy. Only Nodes (Observers) expose this endpoint.
:::

## <span class="badge badge-primary">GET</span> **Get P2P Status**

`http://localhost:8080/node/p2pstatus`

This endpoint allows one to query the P2P status of the Node.

<!--DOCUSAURUS_CODE_TABS-->

<!--Request-->

<!--Response-->

🟢 200: OK

P2P status retrieved successfully.

```
{
  "metrics": {
    "erd_p2p_cross_shard_observers": "...",
    "erd_p2p_cross_shard_validators": "...",
    "erd_p2p_intra_shard_observers": "...",
    "erd_p2p_intra_shard_validators": "...",
    "erd_p2p_num_connected_peers_classification": "...",
    "erd_p2p_num_receiver_peers_fast_reacting": 2,
    "erd_p2p_num_receiver_peers_out_of_specs": 2,
    "erd_p2p_num_receiver_peers_slow_reacting": 13,
    "erd_p2p_peak_num_receiver_peers_fast_reacting": 8,
    "erd_p2p_peak_num_receiver_peers_out_of_specs": 8,
    "erd_p2p_peak_num_receiver_peers_slow_reacting": 13,
    "erd_p2p_peak_peer_num_processed_messages_fast_reacting": 3,
    "erd_p2p_peak_peer_num_processed_messages_out_of_specs": 3,
    "erd_p2p_peak_peer_num_processed_messages_slow_reacting": 8,
    "erd_p2p_peak_peer_num_received_messages_fast_reacting": 3,
    "erd_p2p_peak_peer_num_received_messages_out_of_specs": 3,
    "erd_p2p_peak_peer_num_received_messages_slow_reacting": 8,
    "erd_p2p_peak_peer_size_processed_messages_fast_reacting": 1291,
    "erd_p2p_peak_peer_size_processed_messages_out_of_specs": 1291,
    "erd_p2p_peak_peer_size_processed_messages_slow_reacting": 4363,
    "erd_p2p_peak_peer_size_received_messages_fast_reacting": 1291,
    "erd_p2p_peak_peer_size_received_messages_out_of_specs": 1291,
    "erd_p2p_peak_peer_size_received_messages_slow_reacting": 4363,
    "erd_p2p_peer_info": "...",
    "erd_p2p_peer_num_processed_messages_fast_reacting": 1,
    "erd_p2p_peer_num_processed_messages_out_of_specs": 1,
    "erd_p2p_peer_num_processed_messages_slow_reacting": 5,
    "erd_p2p_peer_num_received_messages_fast_reacting": 1,
    "erd_p2p_peer_num_received_messages_out_of_specs": 1,
    "erd_p2p_peer_num_received_messages_slow_reacting": 5,
    "erd_p2p_peer_size_processed_messages_fast_reacting": 289,
    "erd_p2p_peer_size_processed_messages_out_of_specs": 289,
    "erd_p2p_peer_size_processed_messages_slow_reacting": 2711,
    "erd_p2p_peer_size_received_messages_fast_reacting": 289,
    "erd_p2p_peer_size_received_messages_out_of_specs": 289,
    "erd_p2p_peer_size_received_messages_slow_reacting": 2711,
    "erd_p2p_unknown_shard_peers": "..."
  }
}
```

<!--END_DOCUSAURUS_CODE_TABS-->


:::important
This endpoint is not available on the Proxy. Only Nodes (Observers) expose this endpoint.
:::

## <span class="badge badge-primary">GET</span> **Get Peer Information**

`http://localhost:8080/node/peerinfo`

This endpoint allows one to query specific information about its peers.

<!--DOCUSAURUS_CODE_TABS-->

<!--Request-->

<!--Response-->

🟢 200: OK

Peer info retrieved successfully.

```
{
  "info": [
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "",
      "peertype": "observer",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21100",
        "/ip4/127.0.0.1/tcp/21100",
        "/ip4/192.168.2.104/tcp/21100",
        "/ip4/172.17.0.1/tcp/21100"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "",
      "peertype": "unknown",
      "addresses": [
        "/ip4/127.0.0.1/tcp/9999",
        "/ip4/127.0.0.1/tcp/9999",
        "/ip4/192.168.2.104/tcp/9999",
        "/ip4/172.17.0.1/tcp/9999"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/192.168.2.104/tcp/21504",
        "/ip4/192.168.2.104/tcp/21504",
        "/ip4/172.17.0.1/tcp/21504",
        "/ip4/127.0.0.1/tcp/21504"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21503",
        "/ip4/172.17.0.1/tcp/21503",
        "/ip4/127.0.0.1/tcp/21503",
        "/ip4/192.168.2.104/tcp/21503"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21502",
        "/ip4/127.0.0.1/tcp/21502",
        "/ip4/192.168.2.104/tcp/21502",
        "/ip4/172.17.0.1/tcp/21502"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/127.0.0.1/tcp/21507",
        "/ip4/127.0.0.1/tcp/21507",
        "/ip4/192.168.2.104/tcp/21507",
        "/ip4/172.17.0.1/tcp/21507"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21501",
        "/ip4/192.168.2.104/tcp/21501",
        "/ip4/172.17.0.1/tcp/21501",
        "/ip4/127.0.0.1/tcp/21501"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21508",
        "/ip4/127.0.0.1/tcp/21508",
        "/ip4/192.168.2.104/tcp/21508",
        "/ip4/172.17.0.1/tcp/21508"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21506",
        "/ip4/127.0.0.1/tcp/21506",
        "/ip4/192.168.2.104/tcp/21506",
        "/ip4/172.17.0.1/tcp/21506"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "",
      "peertype": "observer",
      "addresses": [
        "/ip4/127.0.0.1/tcp/38188",
        "/ip4/192.168.2.104/tcp/38188",
        "/ip4/172.17.0.1/tcp/38188"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21505",
        "/ip4/127.0.0.1/tcp/21505",
        "/ip4/192.168.2.104/tcp/21505",
        "/ip4/172.17.0.1/tcp/21505"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "",
      "peertype": "observer",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21102",
        "/ip4/127.0.0.1/tcp/21102",
        "/ip4/192.168.2.104/tcp/21102",
        "/ip4/172.17.0.1/tcp/21102"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "...",
      "peertype": "validator",
      "addresses": [
        "/ip4/172.17.0.1/tcp/21500",
        "/ip4/127.0.0.1/tcp/21500",
        "/ip4/192.168.2.104/tcp/21500",
        "/ip4/172.17.0.1/tcp/21500"
      ]
    },
    {
      "isblacklisted": false,
      "pid": "...",
      "pk": "",
      "peertype": "observer",
      "addresses": [
        "/ip4/192.168.2.104/tcp/21101",
        "/ip4/192.168.2.104/tcp/21101",
        "/ip4/172.17.0.1/tcp/21101",
        "/ip4/127.0.0.1/tcp/21101"
      ]
    }
  ]
}
```

<!--END_DOCUSAURUS_CODE_TABS-->

:::important
This endpoint is not available on the Proxy. Only Nodes (Observers) expose this endpoint.
:::