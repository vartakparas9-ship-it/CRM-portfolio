Company artwork for the AI Deal Intelligence results grid.
================================================================

Save each building photo into THIS folder using the exact filename below.
The dashboard picks it up automatically — no code change needed.
Any company without a file here draws a generated skyline tile instead.

Square images work best (they are cropped to a 32px circle).

    acme-grp.png
    apex-retail.png
    brightwave-media.png
    capgemini-ltd.png
    cobalt-logistics.png
    kotak-mahindra.png
    northwind-systems.png
    nova-enterprises.png
    united-industries.png
    vertex-health.png

Naming rule: company name, lowercased, spaces and punctuation replaced
with hyphens, ".png" on the end.

Using .jpg or a different filename? Add an override in CRM-Deals-Dashboard.html
in the COMPANY_IMG map (search for "COMPANY_IMG_DIR"):

    var COMPANY_IMG = {
      'Acme Grp': 'assets/companies/acme.jpg'
    };

NOTE: opening the dashboard via file:// works in Firefox, but Chrome and Edge
block local image loads from a file:// page in some configurations. If the
tiles stay generated there, serve the folder over http instead, e.g.:

    python -m http.server 8000

then open http://localhost:8000/CRM-Deals-Dashboard.html
