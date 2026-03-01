# Tricount Exporter

Export your Tricount transactions to CSV, Excel, or Sesterce-compatible format.

## Installation

```bash
git clone https://github.com/MrNachoX/tricount-downloader.git
cd tricount-downloader
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage

```bash
bash run.sh
```

When prompted, paste your Tricount URL (e.g. `https://tricount.com/tISWyMCgrIMgFuxudZ`) or just the key (e.g. `tISWyMCgrIMgFuxudZ`).

> To find your key: open your Tricount, share it via a public link, and copy the part after `https://tricount.com/`.

## Output

A CSV file named `Transactions {Tricount Title}.csv` will be created in the current directory.

## Optional exports

To enable additional exports, uncomment the relevant lines at the bottom of `main.py`:

- `handler.write_to_excel(...)` — export to Excel
- `handler.write_to_sesterce_csv(...)` — export to Sesterce-compatible CSV
- `handler.download_attachments(...)` — download all receipt attachments
