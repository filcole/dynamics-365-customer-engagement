---
title: List KPI Types for a Hub (ARM) (Dynamics 365 Customer Insights SDK) | MicrosoftDocs
description: Lists the KPI type definitions for a Hub.
keywords: Customer Insights; ARM API; KPI; list
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.date: 05/17/2017
ms.topic: reference
ms.service: customer-insights 
ms.assetid: 4b986c28-da82-42e6-86d4-fcc8f3920006
---

List KPI Types for a Hub (ARM)
============================

[!include[pre release disclaimer](../../../includes/cc-beta-prerelease-disclaimer.md)]

Lists the [KPI](../types/kpi.md) type definitions for the specified Hub.

## Request  
 The request is constructed as follows:

|**HTTP Verb**|**Request URI**|
|-------------|---------------|
|GET|`https://management.azure.com/subscriptions/<subId>/resourceGroups/<rgName>/providers/Microsoft.CustomerInsights/hubs/<hubName>/kpi?api-version=2017-04-26`|
| | |

### URI Parameters

|**URI Parameter**|**Required**|**Description**|
| --------------- | ---------- | ------------- |
|subId|Yes|Subscription ID|
|rgName|Yes|Azure region name|
|hubName|Yes|Name of your Customer Insights Hub|
| | | |


## Response  
 The response includes a standard HTTP status code, a set of standard response headers, and a response body.

#### Response Body  

A collection of key performance indicator information, including [KPI](../types/kpi.md) type definitions, in the following format:

```{json}  
{
   'value':'[
    {
        'id':'/subscriptions/<subId>/resourceGroups/<rgName>/providers/Microsoft.CustomerInsights/hubs/<hubName>/kpi/<kpiName>'
        'name':'<hubName>/<kpiName>,
        'type':'Microsoft.CustomerInsights/hubs/kpi',
        'properties' : <KPI-Definition>
    },
    {
        'id':'/subscriptions/<subId>/resourceGroups/<rgName>/providers/Microsoft.CustomerInsights/hubs/<hubName>/kpi/<kpiName>'
        'name':'<hubName>/<kpiName>,
        'type':'Microsoft.CustomerInsights/hubs/kpi',
        'properties' : <KPI-Definition>
    } ]',
   'nextLink':'NextLink'
  }

```  

