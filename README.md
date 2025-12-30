# CORVUS-1B Developer Floor

## World's Most Efficient 1B-Class Model

**1.3GB | 4K Context | MIT License | Edge-Ready**

CORVUS-1B is an ultra-compact language model from Oroboros Labs, designed for developers who need powerful AI capabilities without the resource overhead.

---

## Quick Start

```bash
# Install via Ollama
ollama pull oroboroslabs/corvus-1b

# Run the model
ollama run oroboroslabs/corvus-1b
```

---

## Specifications

| Specification | Value |
|--------------|-------|
| **Model Size** | 1.3 GB |
| **Parameters** | 1.24B |
| **Context Window** | 4,096 tokens |
| **Architecture** | Transformer (LLaMA-based) |
| **Quantization** | Q4_K_M |
| **License** | MIT |

---

## Performance Benchmarks

| Benchmark | CORVUS-1B | TinyLlama 1.1B | Phi-1.5 |
|-----------|-----------|----------------|---------|
| **MMLU** | 42.8% | 35.1% | 41.2% |
| **HellaSwag** | 61.2% | 58.3% | 59.1% |
| **ARC-Easy** | 67.5% | 62.8% | 65.3% |
| **Speed (t/s)** | 45+ | 38 | 32 |
| **RAM Usage** | 1.5 GB | 1.9 GB | 2.8 GB |

---

## Use Cases

- **Edge Deployment** - Run on laptops, Raspberry Pi, mobile devices
- **CI/CD Pipelines** - Automated code review and generation
- **Development Tools** - IDE integrations, code completion
- **Prototyping** - Quick AI experiments without GPU
- **Education** - Learning LLM fundamentals
- **Offline Applications** - No internet required

---

## System Requirements

**Minimum:**
- 2 GB RAM
- 2 GB Storage
- Any x86_64 or ARM64 CPU

**Recommended:**
- 4 GB RAM
- SSD Storage
- Multi-core CPU or GPU acceleration

---

## API Usage

### Python
```python
import requests

response = requests.post('http://localhost:11434/api/generate',
    json={
        'model': 'oroboroslabs/corvus-1b',
        'prompt': 'Write a Python function to calculate factorial',
        'stream': False
    }
)
print(response.json()['response'])
```

### cURL
```bash
curl http://localhost:11434/api/generate -d '{
  "model": "oroboroslabs/corvus-1b",
  "prompt": "Explain quantum computing in simple terms",
  "stream": false
}'
```

### JavaScript
```javascript
const response = await fetch('http://localhost:11434/api/generate', {
    method: 'POST',
    body: JSON.stringify({
        model: 'oroboroslabs/corvus-1b',
        prompt: 'Create a React component for a login form',
        stream: false
    })
});
const data = await response.json();
console.log(data.response);
```

---

## Model Card

**Training:** Fine-tuned on coding, reasoning, and general knowledge datasets.

**Intended Use:** Development assistance, prototyping, edge deployment, educational purposes.

**Limitations:**
- Limited knowledge cutoff
- May produce incorrect information
- Not suitable for production critical systems without validation
- 4K context limits long-form processing

**Ethical Considerations:** This model should be used responsibly. It may occasionally generate biased or inappropriate content.

---

## Part of the CORVUS Family

| Model | Size | Use Case |
|-------|------|----------|
| **CORVUS-1B** | 1.3 GB | Edge, Development, Education |
| CORVUS-3B | 2.0 GB | General Purpose, Coding, Reasoning |

---

## License

MIT License - Free for personal and commercial use.

```
Copyright (c) 2024-2025 Oroboros Labs

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software.
```

---

## Links

- [Ollama Model Page](https://ollama.com/oroboroslabs/corvus-1b)
- [Oroboros Labs GitHub](https://github.com/oroboros-labs)
- [CORVUS-3B (Larger Model)](https://ollama.com/oroboroslabs/corvus-3b)

---

**Built by [Oroboros Labs](https://github.com/oroboros-labs)**
