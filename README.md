# gitlint

This repository provides an environment to build the latest gitlint image.

## Getting Started

### Using the Latest Image

```bash
docker pull docker.pkg.github.com/tommyheavenly7/gitlint/gitlint:latest
```

Add the alias setting into `.bashrc`:

```bash
# .bashrc
alias gitlint='docker run --rm -ti -v $(pwd):/git docker.pkg.github.com/tommyheavenly7/gitlint/gitlint:latest'
```

### Setting Up the Build Environment

```bash
source .bashrc
```

#### Login Image Repository

```bash
echo ${GH_TOKEN} | docker login docker.pkg.github.com -u tommyheavenly7 --password-stdin
```

#### Build Image locally

```bash
docker build -t docker.pkg.github.com/tommyheavenly7/gitlint/gitlint:latest ./docker/gitlint
```

#### Push Image to Remote

```bash
docker push docker.pkg.github.com/tommyheavenly7/gitlint/gitlint:latest
```
