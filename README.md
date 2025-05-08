# Swagger Dark Mode

A simple CSS based dark mode for Swagger. No packages or dependencies required.

## Implmentation

Use it like this:

[Tutorial](https://www.youtube.com/watch?v=xvFZjo5PgG0)

```
SwaggerModule.setup('dark-mode-docs', app, generatedDocs, {
    useGlobalPrefix: true,
    customSiteTitle: 'No Mas Flashbangs',
    customCss: `
      /* Main background and text */
      body {
        background-color: #1a1a1a;
        color: #f0f0f0 !important;
      }

      .swagger-ui {
        background-color: #1a1a1a;
        color: #f0f0f0 !important;
      }

      /* Force ALL text to be white */
      .swagger-ui *,
      .swagger-ui .opblock-tag,
      .swagger-ui .opblock .opblock-summary-operation-id,
      .swagger-ui .opblock .opblock-summary-path,
      .swagger-ui .opblock .opblock-summary-path span,
      .swagger-ui .opblock .opblock-summary-description,
      .swagger-ui .model-title,
      .swagger-ui label,
      .swagger-ui span,
      .swagger-ui h1, .swagger-ui h2, .swagger-ui h3, .swagger-ui h4, .swagger-ui h5, .swagger-ui h6,
      .swagger-ui .parameter__name,
      .swagger-ui .parameter__type,
      .swagger-ui table thead tr th,
      .swagger-ui table tbody tr td,
      .swagger-ui .response-col_status,
      .swagger-ui .response-col_description,
      .swagger-ui .tab li,
      .swagger-ui section.models h4,
      .swagger-ui section.models h5,
      .swagger-ui .servers > label {
        color: #f0f0f0 !important;
      }

      /* Override any SVGs or special elements */
      .swagger-ui svg {
        fill: #f0f0f0 !important;
      }

      .swagger-ui .scheme-container {
        background-color: #1a1a1a;
      }

      .swagger-ui .opblock .opblock-section-header {
        background-color: #1a1a1a;
      }

      .swagger-ui .dialog-ux .modal-ux {
        background-color: #1a1a1a;
      }

      /* Operation blocks */
      .swagger-ui .opblock {
        background-color: #2d2d2d;
        border-color: #444;
      }

      /* Input fields */
      .swagger-ui input[type=text],
      .swagger-ui textarea {
        background-color: rgb(12, 12, 12);
        color: white !important;
      }

      .swagger-ui input,
      .swagger-ui select,
      .swagger-ui textarea {
        background-color: #333;
        color: white !important;
      }

      /* Code blocks */
      .swagger-ui .highlight-code,
      .swagger-ui .microlight {
        background-color:rgb(69, 69, 68) !important;
        color: #f8f8f2 !important;
      }
    `,
    swaggerOptions: {
      defaultModelsExpandDepth: -1,
      docExpansion: 'none',
      filter: true,
      displayRequestDuration: true,
    },
  });
```
