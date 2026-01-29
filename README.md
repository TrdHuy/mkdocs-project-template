# Privacy Sandbox Docs (POC)

Dự án Proof-of-Concept tài liệu sử dụng MkDocs + mkdocs-material. Tài liệu được viết bằng Markdown và build ra static HTML.

## Yêu cầu
- Linux
- Python 3
- Không cài package Python global

## Setup Python venv
```bash
cd privacy-sandbox-docs
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
```

## Cài đặt dependency
```bash
pip install mkdocs mkdocs-material
```

## Chạy preview local
```bash
mkdocs serve
```
Truy cập: http://127.0.0.1:8000

## Build static site
```bash
mkdocs build
```
Output nằm trong thư mục `site/` (static HTML hoàn chỉnh).

## GitHub Pages (CI)
Workflow đã được cấu hình tại `.github/workflows/deploy-pages.yml`.

Cần bật GitHub Pages:
- Vào Settings → Pages
- Build and deployment: chọn **GitHub Actions**

Sau khi push lên nhánh `main`, site sẽ được deploy tự động.
