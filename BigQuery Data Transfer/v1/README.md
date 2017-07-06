﻿![BigQuery Data Transfer Service API](http://www.google.com/images/icons/product/search-32.gif)

#Unoffical BigQuery Data Transfer Service API v1 Samples for .NET  

##API Description
=============

Transfers data from partner SaaS applications to Google BigQuery on a scheduled, managed basis.

[Offical Documentation](https://cloud.google.com/bigquery/)

##Sample Description
=============

These samples show how to access the [BigQuery Data Transfer Service API v1](https://cloud.google.com/bigquery/) with the Offical [Google .Net client library](https://github.com/google/google-api-dotnet-client)

Tutorials to go along with some of these samples can be found on [www.daimto.com](http://www.daimto.com/)

#Developer Documentation

* [Google API client Library for .NET - Get Started](https://developers.google.com/api-client-library/dotnet/get_started)

* [Supported APIs](https://developers.google.com/api-client-library/dotnet/apis/)

##Installation
=================================

NuGet package:

Location: [NuGet Google.Apis.BigQueryDataTransfer.v1](https://www.nuget.org/packages/Google.Apis.BigQueryDataTransfer.v1)
Install Command: PM>  Install-Package Google.Apis.BigQueryDataTransfer.v1

```
PM> Install-Package Google.Apis.BigQueryDataTransfer.v1
```

##Usage
=================================

OAuth2
```
var keyFileLocation = @"C:\Users\Daimto\Documents\DaimtoTestEverythingCredentials\Diamto Test Everything Project-29e50502c19b.json";
var user = System.Security.Principal.WindowsIdentity.GetCurrent().Name;
var scopes = new String[] { Google.Apis.BigQueryDataTransfer.v1.BigQueryDataTransferService.Scope.BigQueryDataTransferReadonly };
var service = GoogleSamplecSharpSample.BigQueryDataTransferv1.Auth.Oauth2Example.GetBigQueryDataTransferService(keyFileLocation, user, scopes);
```
Public API Key
```
var apiKey = "XXXX";
var servicePublicKey = GoogleSamplecSharpSample.BigQueryDataTransferv1.Auth.ApiKeyExample.GetService(apiKey);
```
Service Account
```
var serviceAccountKeyFileLocation = @"C:\Users\Daimto\Documents\DaimtoTestEverythingCredentials\Diamto Test Everything Project-29e50502c19b.json";
var serviceAccountEmail = "googledrivemirrornas@daimto-tutorials-101.iam.gserviceaccount.com";
var scopes = new String[] { Google.Apis.BigQueryDataTransfer.v1.BigQueryDataTransferService.Scope.Calendar };            
var serviceAccountService = GoogleSamplecSharpSample.BigQueryDataTransferv1.Auth.ServiceAccountExample.AuthenticateServiceAccount(serviceAccountKeyFileLocation, serviceAccountEmail, scopes);
```