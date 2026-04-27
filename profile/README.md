# RFID Self-Checkout

[![Backend CI](https://github.com/rfidcheckout/rfid-totem-backend/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/rfidcheckout/rfid-totem-backend/actions/workflows/ci.yml)
[![Frontend CI](https://github.com/rfidcheckout/rfid-totem-frontend/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/rfidcheckout/rfid-totem-frontend/actions/workflows/ci.yml)

Sistema autônomo de ponto de venda para varejo, baseado em leitura RFID para identificação de produtos sem necessidade de leitura individual de códigos de barras.

## Arquitetura

O sistema opera em um **totem físico** com os seguintes componentes:

- **Backend** — monolito modular em Go (Chi + Huma), PostgreSQL local, comunicação real-time via WebSocket
- **Frontend** — aplicação Angular touch-first servida como assets estáticos pelo backend
- **Hardware** — leitor RFID (Yanpodo YRM100), trava magnética (relé GPIO), câmera (ffmpeg + V4L2), pinpad de pagamento
- **Integração** — sincronização com ERP Sysok para catálogo de produtos e fechamento fiscal

## Repositórios

| Repositório | Descrição |
|---|---|
| [rfid-architecture](https://github.com/rfidcheckout/rfid-architecture) | ADRs, padrões, roadmap e documentação cross-repo |
| [rfid-totem-backend](https://github.com/rfidcheckout/rfid-totem-backend) | Monolito Go — API REST, WebSocket, hardware, checkout |
| [rfid-totem-frontend](https://github.com/rfidcheckout/rfid-totem-frontend) | Aplicação Angular — interface do totem |

## Status

🚧 Em desenvolvimento — MVP

## Stack

| Camada | Tecnologia |
|---|---|
| Linguagem backend | Go |
| Framework HTTP | Chi + Huma |
| Banco de dados | PostgreSQL (local) |
| Acesso a dados | sqlc + pgx + goose |
| API | REST (OpenAPI 3.1) + WebSocket |
| Frontend | Angular + Angular Material |
| Hardware | periph.io (GPIO), go.bug.st/serial (USB) |
| Deploy | Binário único + systemd |
