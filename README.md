# ALICE-Space SaaS

Deep-space communication and trajectory control API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Space |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/trajectory` | 軌道計算 |
| `POST /api/v1/communicate` | 深宇宙通信シミュレーション |
| `GET  /api/v1/bodies` | 天体データベース |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
