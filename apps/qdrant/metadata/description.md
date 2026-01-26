# Qdrant - Vector Database

Qdrant (read: *quadrant*) is a vector similarity search engine and vector database. It provides a production-ready service with a convenient API to store, search, and manage points—vectors with an additional payload.

## Features

- **High Performance** - Written in Rust for speed and reliability even under high load
- **Filtering & Payload** - Attach JSON payloads to vectors and filter based on payload values
- **Hybrid Search** - Support for both dense and sparse vectors
- **Vector Quantization** - Reduce RAM usage by up to 97%
- **Distributed Deployment** - Horizontal scaling with sharding and replication
- **REST & gRPC API** - Easy integration with any programming language

## Poorten

- **6333** - REST API (hoofd interface)
- **6334** - gRPC API (voor snellere productie-tier searches)

## Gebruik

### REST API

De Qdrant REST API is beschikbaar op `http://<your-server>:6333`. 

Voorbeeld om een collectie aan te maken:

```bash
curl -X PUT 'http://localhost:6333/collections/my_collection' \
  -H 'Content-Type: application/json' \
  --data-raw '{
    "vectors": {
      "size": 384,
      "distance": "Cosine"
    }
  }'
```

### Web UI

Qdrant heeft een ingebouwde Web UI beschikbaar op `http://<your-server>:6333/dashboard`

## Client Libraries

- Python: `pip install qdrant-client`
- JavaScript/TypeScript: `npm install @qdrant/js-client-rest`
- Go, Rust, .NET, Java clients zijn ook beschikbaar

## Documentatie

- [Officiële Documentatie](https://qdrant.tech/documentation/)
- [GitHub Repository](https://github.com/qdrant/qdrant)
- [API Reference](https://qdrant.github.io/qdrant/redoc/index.html)

## Beveiliging

Als je een API key hebt ingesteld, voeg deze toe aan je requests:

```bash
curl -X GET 'http://localhost:6333/collections' \
  -H 'api-key: <your-api-key>'
```
