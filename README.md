# n8n with Zint

This Repository contains the Dockerfile and docker-entrypont.sh from https://github.com/n8n-io/n8n/tree/master/docker/images/n8n

Zint is added to the image so you can generate qr Codes and Barcodes directly in n8n from command line.

Build the image with the following command: `sudo docker build -t n8n:1.58.2 --build-arg N8N_VERSION=1.58.2 .` but replace the n8n version with the current version.

Example code for the command line node: `zint -b 58 --bg=000000 --eci=26 -d 'This data as qr code' --esc --fg=FFFFFF --quietzones -o Filename.svg`

You can find some examples in the folder Beispiele. The workflows were uploaded as JSON. In n8n you can import them directly into a new or an existing workflow.

German: Im Ordner Beispiele sind einige Workflows als JSON hochgeladen. Diese können direkt in einen neuen oder bestehenden Workflow importiert werden.
