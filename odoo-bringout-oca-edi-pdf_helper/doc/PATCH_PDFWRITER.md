# PyPDF2 Compatibility Patch - PDF Helper (EDI)

## Overview

This package benefits from the PyPDF2 compatibility fixes implemented in the `oca-ocb-base` package. The pdf_helper module uses `OdooPdfFileWriter` and `OdooPdfFileReader` classes that are automatically compatible with PyPDF2 3.0.0+ through the main compatibility layer.

## Problem

In PyPDF2 3.0.0, several classes and methods were deprecated and removed:
- `PdfFileWriter` → `PdfWriter`
- `PdfFileReader` → `PdfReader`
- Various method names changed (e.g., `addPage()` → `add_page()`)

## Affected Functionality

The pdf_helper module uses PyPDF2 indirectly through:
- `OdooPdfFileWriter` for embedding XML attachments in PDFs
- `OdooPdfFileReader` for extracting XML files from PDF documents
- XML-to-PDF embedding for EDI workflows
- PDF parsing and attachment processing

## Solution

**This package requires NO direct patches** because it uses:
1. `OdooPdfFileWriter` from `odoo.tools.pdf` (oca-ocb-base)
2. `OdooPdfFileReader` from `odoo.tools.pdf` (oca-ocb-base)

The main compatibility layer in `oca-ocb-base` handles all PyPDF2 version compatibility automatically.

## Files Using PyPDF2

### `pdf_helper/utils.py`
- Imports `PdfReadError` with compatibility handling
- Uses `OdooPdfFileReader` (automatically compatible)

### `pdf_helper/models/helper.py`  
- Uses `OdooPdfFileWriter` and `OdooPdfFileReader` (automatically compatible)
- Calls methods like `cloneReaderDocumentRoot()` and `addAttachment()`

## Implementation Details

**No code changes needed** in this package. Compatibility is achieved through:

1. **Dependency**: Requires `oca-ocb-base` with `pdfwrite` branch
2. **Automatic compatibility**: `OdooPdfFileWriter`/`OdooPdfFileReader` handle all PyPDF2 version differences
3. **Import handling**: Exception imports handle both old and new PyPDF2 locations

## Testing

The compatibility has been verified with:
- PyPDF2 3.0.0+ (new API)
- PyPDF2 2.x (old API)
- XML embedding in PDFs
- XML extraction from PDFs
- EDI document processing workflows

## Branch Information

- **Branch**: `pdfwrite`
- **Based on**: Current master branch
- **Type**: Dependency compatibility (no direct patches)
- **Impact**: Automatic compatibility through oca-ocb-base dependency

## Dependencies

**CRITICAL**: This package requires:
- `oca-ocb-base` package on `pdfwrite` branch
- The main PyPDF2 compatibility layer must be active

## Author

- **Developer**: Ernad Husremović (hernad@bring.out.ba)
- **Company**: bring.out.doo Sarajevo
- **Date**: 2025-09-02

## Related Issues

This documentation addresses PyPDF2 compatibility for:
- EDI XML embedding workflows
- PDF attachment processing
- Electronic document interchange

## Installation

1. Ensure `oca-ocb-base` is using the `pdfwrite` branch
2. Use this package's `pdfwrite` branch (for documentation compliance)
3. No additional installation steps required

## Future Considerations

- Monitor oca-ocb-base compatibility updates
- Test EDI workflows with future PyPDF2 versions
- Consider direct PyPDF2 usage optimization if needed