# Grafana PDF using Puppeteer

Generate pdf for grafana dashboards using nodejs and puppeteer.

I took the base code from 
https://gist.github.com/svet-b/1ad0656cd3ce0e1a633e16eb20f66425

It was generating blank panels after certain point when dashboard is tall. This code addresses this issue.

## Examples
Environment: Set the Grafana server URL, username, and password, and the output filename as environment variables.

``` sh
export GF_DASH_URL="http://localhost:3000/d/x3g4Wx5ik/new-dashboard?kiosk"
export GF_USER=pdf_export
export GF_PASSWORD=StrongPassword1
export OUTPUT_PDF=output/output.pdf

# Now export to PDF by calling the NodeJS script with the corresponding arguments:

node grafana_pdf.js $GF_DASH_URL $GF_USER:$GF_PASSWORD $OUTPUT_PDF

node grafana_pdf.js "http://localhost:3000/d/7ps_KoFMk?orgId=1&from=1602513421982&to=1602513601734" admin:admin output/grafana_dash.pdf

```
