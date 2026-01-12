# CrisLink MQTT Schema v1.0

## Topics

### Node state

crislink/node/<nodeId>/state
### Heartbeat

crislink/node/<nodeId>/heartbeat
### Commands

crislink/cmd/<nodeId>/set
crislink/cmd/broadcast

---

## State payload (example)

```json
{
  "nodeId": "CL-N100",
  "type": "lighthouse",
  "state": "GREEN_SOLID",
  "ts": "2026-01-12T07:30:00Z"
}


Rules

JSON only
UTF-8
nodeId is mandatory
CLP ignores unknown fields

