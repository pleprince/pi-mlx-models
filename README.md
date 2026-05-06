# pi-mlx-models

Local MLX models for Pi (Apple Silicon).

## Features

- `/mlx-init` — installs runtime (`python venv` + `mlx-lm`)
- `/mlx-start` — opens interactive preset selector (or accepts model id)
- `/mlx-stop` — stops local MLX server
- Single-stage startup progress UI with live warm-up timer
- Hides models until the server is actually ready

## Install

```bash
pi install npm:pi-mlx-models
```

Or from GitHub:

```bash
pi install git:github.com/vmarinogg/pi-mlx-models
```

## Usage

```bash
/mlx-init
/mlx-start
```

`/mlx-start` with no args opens a selector.
You can also pass a value directly:

```bash
/mlx-start qwen3_4b
/mlx-start mlx-community/Qwen3-4B-Instruct-2507-4bit
```

## Requirements

- macOS on Apple Silicon
- Python 3.10–3.13

## Development

```bash
npm install
npm run build
```

Pi package manifest is defined in `package.json`:

- `pi.extensions: ["dist/index.js"]`

## License

MIT
