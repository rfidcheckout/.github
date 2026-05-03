# RFID Self-Checkout

Sistema autônomo de ponto de venda para varejo, baseado em leitura RFID para identificação instantânea de produtos — sem necessidade de leitura individual de códigos de barras.

> **Status:** Em desenvolvimento — [Project Board](https://github.com/orgs/rfidcheckout/projects/3)

## Repositórios

| | Repositório | Descrição |
|:---:|---|---|
| | [`rfid-architecture`](https://github.com/rfidcheckout/rfid-architecture) | ADRs, padrões, roadmap e documentação cross-repo |
| [![CI](https://github.com/rfidcheckout/rfid-totem-backend/actions/workflows/ci.yml/badge.svg)](https://github.com/rfidcheckout/rfid-totem-backend/actions/workflows/ci.yml) | [`rfid-totem-backend`](https://github.com/rfidcheckout/rfid-totem-backend) | Monolito Go — API REST, WebSocket, hardware, checkout |
| [![CI](https://github.com/rfidcheckout/rfid-totem-frontend/actions/workflows/ci.yml/badge.svg)](https://github.com/rfidcheckout/rfid-totem-frontend/actions/workflows/ci.yml) | [`rfid-totem-frontend`](https://github.com/rfidcheckout/rfid-totem-frontend) | Angular — interface touch-first do totem |

## Stack

| Camada | Tecnologia |
|---|---|
| Backend | Go · Chi + Huma · REST (OpenAPI 3.1) + WebSocket |
| Dados | PostgreSQL · sqlc · pgx · goose |
| Frontend | Angular · Angular Material |
| Deploy | Binário único + systemd |
