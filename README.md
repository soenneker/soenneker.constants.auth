[![](https://img.shields.io/nuget/v/Soenneker.Constants.Auth.svg?style=for-the-badge)](https://www.nuget.org/packages/Soenneker.Constants.Auth/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.constants.auth/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.constants.auth/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/Soenneker.Constants.Auth.svg?style=for-the-badge)](https://www.nuget.org/packages/Soenneker.Constants.Auth/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.constants.auth/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.constants.auth/actions/workflows/codeql.yml)

# Soenneker.Constants.Auth

Provides the conventional `x-api-key` HTTP header name.

## Install

```bash
dotnet add package Soenneker.Constants.Auth
```

## Usage

```csharp
using Soenneker.Constants.Auth;

httpClient.DefaultRequestHeaders.Add(AuthConstants.XApiKey, apiKey);
```

`AuthConstants.XApiKey` has the literal value `"x-api-key"`. HTTP header names are case-insensitive; the lowercase spelling is provided for consistency across clients, middleware, and tests.

This package only supplies the header name. It does not validate credentials or configure an authentication scheme. Treat the associated header value as a secret and exclude it from logs and telemetry.
