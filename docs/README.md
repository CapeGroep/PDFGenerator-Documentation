# PDF Generator Module Overview

## Introduction

The PDF Generator is a comprehensive solution developed by Cape Group for generating PDF documents directly from your Mendix application. This powerful tool offers flexibility and robust features to meet diverse PDF generation needs.

## Generation Methods

The module offers multiple methods to generate PDFs:

1. **Client-Side Generation**
   - Uses HTML2PDF
   - Two types available:
     a. Normal (Recommended for most cases)
     b. Legacy (For specific use cases)

2. **Server-Side Generation**
   - Uses Puppeteer & Chromium
   - Requires a license

## Key Features

- Multi-page support
- Custom headers and footers
- Adjustable DPI
- Flexible paper orientation
- Simultaneous generation of multiple PDFs
- Easy-to-use layout templates
- Batch processing (Server-side only)
- Background processing (Server-side only)

## Common Installation Procedure

Regardless of which generation method you choose, follow these steps to set up the PDF Generator module:

1. Implement `USE_ME/ASU_PDFGenerator` in your Mendix application's after-startup microflow.

2. Implement `USE_ME/Configuration/PDFGeneratorConfiguration_Snippet` in your application's configuration page.

3. Run the application and input the license key provided by CAPE Groep. Get the license key (or demo license key) from info@capegroep.nl

## Client-Side Generation

### Normal Type
- Easier to configure
- Suitable for most straightforward PDF generation needs
- Cannot display certain Mendix widgets (e.g., graphs)
- Single page layout per PDF

### Legacy Type
- More complex configuration
- Works with graphs
- Allows different page layouts in one PDF
- More flexible but harder to get right

### Limitations of Client-Side Generation
- Cannot perform batch processing or scheduled processing
- Generates image-based PDFs
- Some widget compatibility issues (Normal type)

## Server-Side Generation

- Supports batch processing and scheduled generation
- Can handle complex Mendix widgets
- Offers higher quality PDFs
- Requires a license
- More robust for generating large numbers of PDFs

## Choosing the Right Method

1. **Use Normal Client-Side** when:
   - You need a simple, straightforward PDF generation
   - You don't need to include complex widgets or multiple layouts

2. **Use Legacy Client-Side** when:
   - You need to include graphs in your PDFs
   - Your PDF requires multiple different page layouts within a single document
   - You're willing to work with a more complex configuration for greater flexibility

3. **Use Server-Side** when:
   - You need batch processing or scheduled PDF generation
   - You're generating large numbers of PDFs
   - You need to include complex Mendix widgets
   - You require higher quality PDFs that are not image-based

## Getting Started

After completing the common installation procedure:

- For Client-Side Normal setup, see: [Setting Up Normal Client-Side PDF Generation](clientside-implementation-guide.md)
- For Client-Side Legacy setup, see: [Setting Up Legacy Client-Side PDF Generator](clientside-legacy-implementation-guide.md)
- For Server-Side setup, see: [Setting Up Server-Side PDF Generation](serverside-implementation-guide.md)

## Licensing

- Client-side generation can be used locally without a license
- Server-side generation requires a license
- Contact info@capegroep.nl for licensing information or to request a demo license

## Support

For further assistance or to report issues, please contact our support team at [info@capegroep.nl].

