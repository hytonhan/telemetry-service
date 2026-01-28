# telemetry-service
Project for a tcp based c++ server that receives telemerty data from a simulated device client and stores it in SQL database and exposes a small REST API to query the data

## Tech stack
- C++17
- TCP: Boost.Asio
- JSON: nlohmann/json
- REST server: cpp-httplib
- Database PostgreSQL + libpqxx
- CMake
- Linux

### Sample telemetry message
```json
{
  "device_id": "sensor-001",
  "timestamp": "2026-01-28T12:45:30Z",
  "signal_strength": -73.4,
  "frequency_hz": 2450000000,
  "latitude": 61.4978,
  "longitude": 23.7610
}
```
### DB Schema
| Column          |	Type             |
|-----------------|------------------|
| id              |	SERIAL / BIGINT  |
| device_id	      | VARCHAR          |
| timestamp	      | TIMESTAMP        |
| signal_strength	| FLOAT            |
| frequency_hz	  | BIGINT           |
| latitude	      | DOUBLE PRECISION |
| longitude	      | DOUBLE PRECISION |
