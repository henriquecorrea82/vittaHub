```mermaid
flowchart TD
  A[Planejamento / Requisitos] --> B[Code]
  B --> C[Pull Request + Review]
  C --> D[CI: Build + Tests]
  D --> E[SAST + Dependency Scan]
  E --> F[Docker Build]
  F --> G[CD: Dev -> Homolog -> Prod]
  G --> H[Monitoramento + Logs]
  H --> I[Auditoria + Resposta a Incidentes]
  I --> J[Melhoria Contínua]

