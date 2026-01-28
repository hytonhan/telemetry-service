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
