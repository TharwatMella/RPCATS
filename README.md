# Cat Breed Information CLI

A command-line application that fetches and displays cat breed information from [The Cat API](https://thecatapi.com/).

## Requirements

- Python 3.14 or later
- [uv](https://docs.astral.sh/uv/)
- Internet access

The project uses [`requests`](https://requests.readthedocs.io/) for HTTP requests. The dependency is declared in `pyproject.toml` and is installed automatically by uv.

## Installation

Clone or download the project, then sync its dependencies:

```bash
uv sync
```

## Usage

Pass a breed name as the positional argument:

```bash
uv run main.py Siamese
```

The breed name must match the name used by The Cat API exactly. The command displays:

- Origin
- Temperament
- Life span
- Weight in pounds
- Breed ID
- Wikipedia link, when available

Example with another breed:

```bash
uv run main.py Bengal
```

If the breed is not found, the application suggests trying another name. Network and API errors are reported with a non-zero exit status.

## API access

The application requests the breed list from:

```text
https://api.thecatapi.com/v1/breeds
```

The API key is sent in the request header by `main.py`. Keep API keys private and rotate the key if it is exposed.
