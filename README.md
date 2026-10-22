 # Cat Breed Information CLI

Fetch and display information about cat breeds using [The Cat API](https://thecatapi.com/).

## Requirements

- Python 3
- `requests`

Install the dependency with:

```bash
uv add requests
```

## Usage

```bash
uv run main.py Siamese
```

Replace `Siamese` with the exact name of another breed. The command displays the breed's origin, temperament, lifespan, weight, ID, and Wikipedia link when available.
