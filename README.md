PDFgen
======

PDFgen is a docker application build to generate pdf documents.
It depends on wkhtmltopdf and has a clean API.

# Install

Make sure you have docker installed and run the following.

```bash
$ docker run -d -p 80:80 nousefreak/pdfgen
```
# Usage

The API accepts a source object containing the url of the page you want.
You can pass along any options via the options object. See the [reference](http://wkhtmltopdf.org/usage/wkhtmltopdf.txt) for all available options.

# Example

```bash
$ curl \
    -H "Accept: application/json" \
    -H "Content-type: application/json" \
    -X POST \
    -d '{"source": {"url": "https://www.google.com"},"options": {"no-background": true}}' \
    http://192.168.99.100:80/
```

