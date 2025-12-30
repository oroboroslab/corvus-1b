# CORVUS-1B Developer Floor Edition

Ultra-efficient 1B-class language model optimized for edge deployment and resource-constrained environments.

## Specifications

| Spec | Value |
|------|-------|
| **Parameters** | 1.24B |
| **Size** | 1.3 GB |
| **Context Window** | 4,096 tokens |
| **Architecture** | LLaMA-based Transformer |
| **Quantization** | Q4_K_M |
| **License** | MIT |

## Performance Benchmarks

| Benchmark | Score |
|-----------|-------|
| MMLU | 42.8% |
| HellaSwag | 61.2% |
| ARC-Easy | 67.5% |
| TruthfulQA | 38.4% |
| Speed (CPU) | 45+ tokens/sec |

## System Requirements

**Minimum:**
- 2 GB RAM
- 2 GB Storage
- Any x86_64 or ARM64 CPU

**Recommended:**
- 4 GB RAM
- SSD Storage
- Multi-core CPU

## Use Cases

- Edge deployment (IoT, embedded systems)
- CI/CD pipelines (code review, PR summaries)
- Local development assistant
- Offline applications
- Educational purposes
- Cost-sensitive deployments

## Quick Start

```bash
ollama run oroboroslabs/corvus-1b
```

## API Example

```python
import requests

response = requests.post('http://localhost:11434/api/generate',
    json={
        'model': 'oroboroslabs/corvus-1b',
        'prompt': 'Write a hello world in Python',
        'stream': False
    }
)
print(response.json()['response'])
```

## Part of the CORVUS Family

| Model | Size | Use Case |
|-------|------|----------|
| **CORVUS-1B** | 1.3 GB | Edge, Development |
| CORVUS-3B | 2.0 GB | General Purpose, Coding |

## Links

- [Landing Page](https://oroboroslab.github.io/corvus-1b/)
- [GitHub](https://github.com/oroboroslab/corvus-1b)
- [Oroboros Labs](https://oroboroslab.github.io)

---
**Built by Oroboros Labs** | MIT License
