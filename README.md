# IntroToPython

> Developer tooling for [IntroToPython](https://github.com/pdeitel/IntroToPython/)

This repository does NOT redistribute example files from the Deitel/Pearson book.
Students must obtain the book and its accompanying materials separately.

Note:
Due to evolving software and incomplete snippets, not all code will run without additional work.
This repo is used to make much of the code runnable or inspectable in VS Code.

## Recommended Installations

- git
- Python
- VS Code (and extensions)

## Developer

This repository provides a professional working environment;
the book examples are added locally.

### 1. Clone this repo

```shell
git clone https://github.com/denisecase/IntroToPython
cd IntroToPython
code .
```

### 2. Obtain the textbook example files

- See the official Deitel repository at <https://github.com/pdeitel/IntroToPython>.
- Copy the book's `examples/` folder into this repository.
- Ensure `examples/` is parallel to the `images/` folder (both in root).

### 3. Install `uv`

### 4. Initialize (Just Once)

```shell
uv self update
uv python pin 3.12
uvx pre-commit install
uvx pre-commit run --all-files

# Windows:
.venv\Scripts\activate

# macOS/Linux:
# source .venv/bin/activate

uv sync --extra dev --extra docs --upgrade
```

### 5. Run Individual Examples

If you see something like this, click "Install".

  ![Popup](./images/install.gif)

Run a file (e.g.,):

```shell
uv run python examples\ch01\RollDieDynamic.py 400 1
uv run python examples\ch11\snippets_ipynb\ch11soundutilities.py
```

If a window pops up, close the window (or if needed, delete the terminal) to continue.

Open Notebooks and Click `Run All`. Select the kernel associated with this repo `.venv`.

### 6. Save Progress (As Needed)

If you update your copy of the examples, you might want to save progress.

```shell
git add -A
# If pre-commit makes changes, re-run `git add -A` before committing.
git commit -m "update"
git push -u origin main
```

## Citation

This repository does not redistribute textbook example files.
If you add the Deitel/Pearson examples locally, please respect the book's copyright
and do not publish or redistribute those files.

[CITATION.cff](./CITATION.cff)

## License

[MIT](./LICENSE)

## Notice

[NOTICE.md](./NOTICE.md)

## UPSTREAM

[UPSTREAM.md](./UPSTREAM.md)

## Annotations

[Annotations.md](./ANNOTATIONS.md)

## SE MANIFEST

[SE_MANIFEST.toml](./SE_MANIFEST.toml)
