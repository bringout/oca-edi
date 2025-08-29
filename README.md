# OCA Edi

This repository contains **42** OCA packages for edi.

## Packages Included (42 packages)

- **odoo-bringout-oca-edi-account_einvoice_generate** - From edi: account_einvoice_generate
- **odoo-bringout-oca-edi-account_invoice_edifact** - From edi: account_invoice_edifact
- **odoo-bringout-oca-edi-account_invoice_export** - From edi: account_invoice_export
- **odoo-bringout-oca-edi-account_invoice_export_job** - From edi: account_invoice_export_job
- **odoo-bringout-oca-edi-account_invoice_facturx** - From edi: account_invoice_facturx
- **odoo-bringout-oca-edi-account_invoice_facturx_py3o** - From edi: account_invoice_facturx_py3o
- **odoo-bringout-oca-edi-account_invoice_ubl** - From edi: account_invoice_ubl
- **odoo-bringout-oca-edi-base_business_document_import** - From edi: base_business_document_import
- **odoo-bringout-oca-edi-base_business_document_import_phone** - From edi: base_business_document_import_phone
- **odoo-bringout-oca-edi-base_ebill_payment_contract** - From edi: base_ebill_payment_contract
- **odoo-bringout-oca-edi-base_edi** - From edi: base_edi
- **odoo-bringout-oca-edi-base_edifact** - From edi: base_edifact
- **odoo-bringout-oca-edi-base_facturx** - From edi: base_facturx
- **odoo-bringout-oca-edi-base_ubl** - From edi: base_ubl
- **odoo-bringout-oca-edi-base_ubl_payment** - From edi: base_ubl_payment
- **odoo-bringout-oca-edi-base_wamas_ubl** - From edi: base_wamas_ubl
- **odoo-bringout-oca-edi-despatch_advice_import** - From edi: despatch_advice_import
- **odoo-bringout-oca-edi-despatch_advice_import_ubl** - From edi: despatch_advice_import_ubl
- **odoo-bringout-oca-edi-framework-account_einvoice_generate** - From edi: framework_account_einvoice_generate
- **odoo-bringout-oca-edi-framework-account_invoice_edifact** - From edi: framework_account_invoice_edifact
- **odoo-bringout-oca-edi-framework-account_invoice_export** - From edi: framework_account_invoice_export
- **odoo-bringout-oca-edi-framework-account_invoice_export_job** - From edi: framework_account_invoice_export_job
- **odoo-bringout-oca-edi-framework-account_invoice_facturx** - From edi: framework_account_invoice_facturx
- **odoo-bringout-oca-edi-framework-account_invoice_facturx_py3o** - From edi: framework_account_invoice_facturx_py3o
- **odoo-bringout-oca-edi-framework-account_invoice_ubl** - From edi: framework_account_invoice_ubl
- **odoo-bringout-oca-edi-framework-base_business_document_import** - From edi: framework_base_business_document_import
- **odoo-bringout-oca-edi-framework-base_business_document_import_phone** - From edi: framework_base_business_document_import_phone
- **odoo-bringout-oca-edi-framework-base_ebill_payment_contract** - From edi: framework_base_ebill_payment_contract
- **odoo-bringout-oca-edi-framework-base_edi** - From edi: framework_base_edi
- **odoo-bringout-oca-edi-framework-base_edifact** - From edi: framework_base_edifact
- **odoo-bringout-oca-edi-framework-base_facturx** - From edi: framework_base_facturx
- **odoo-bringout-oca-edi-framework-base_ubl** - From edi: framework_base_ubl
- **odoo-bringout-oca-edi-framework-base_ubl_payment** - From edi: framework_base_ubl_payment
- **odoo-bringout-oca-edi-framework-base_wamas_ubl** - From edi: framework_base_wamas_ubl
- **odoo-bringout-oca-edi-framework-despatch_advice_import** - From edi: framework_despatch_advice_import
- **odoo-bringout-oca-edi-framework-despatch_advice_import_ubl** - From edi: framework_despatch_advice_import_ubl
- **odoo-bringout-oca-edi-framework-pdf_helper** - From edi: framework_pdf_helper
- **odoo-bringout-oca-edi-framework-sale_order_import** - From edi: framework_sale_order_import
- **odoo-bringout-oca-edi-framework-sale_order_import_edifact** - From edi: framework_sale_order_import_edifact
- **odoo-bringout-oca-edi-pdf_helper** - From edi: pdf_helper
- **odoo-bringout-oca-edi-sale_order_import** - From edi: sale_order_import
- **odoo-bringout-oca-edi-sale_order_import_edifact** - From edi: sale_order_import_edifact


## Installation

Install any package from this category:

```bash
# Install from local directory
pip install packages/oca-edi/PACKAGE_NAME/

# Install in development mode  
pip install -e packages/oca-edi/PACKAGE_NAME/

# Using uv (recommended for speed)
uv add packages/oca-edi/PACKAGE_NAME/
```

## Repository Structure

Each package in this repository follows the standard Odoo addon structure:

```
oca-edi/
├── odoo-bringout-oca-PROJECT-ADDON/
│   ├── ADDON_NAME/           # Complete addon code
│   │   ├── __init__.py
│   │   ├── __manifest__.py
│   │   └── ... (models, views, etc.)
│   ├── pyproject.toml        # Python package configuration
│   └── README.md            # Package documentation
└── ...
```

## Contributing

These packages are maintained as part of the [OCA (Odoo Community Association)](https://github.com/OCA) ecosystem.

## License

Each package maintains its original license as specified in the OCA repositories.
