# open-banking-us-postman
[![](https://raw.githubusercontent.com/Mastercard/open-banking-us-openapi/main/res/logo.png)](https://developer.mastercard.com/product/open-banking/#gh-light-mode-only)
[![](https://raw.githubusercontent.com/Mastercard/open-banking-us-openapi/main/res/logo-dark.png)](https://developer.mastercard.com/product/open-banking/#gh-dark-mode-only)

## Overview

The [Postman](https://www.postman.com/) collection for [Open Banking APIs](https://developer.mastercard.com/open-banking-us/documentation) (🇺🇸) tested using [Newman](https://learning.postman.com/docs/running-collections/using-newman-cli/command-line-integration-with-newman/) and the Test Drive plan.

## Workflows

The following workflow runs the collection and ensures it can be used to consume and test the Open Banking APIs:

[![](https://github.com/Mastercard/open-banking-us-postman/actions/workflows/newman.yml/badge.svg)](https://github.com/Mastercard/open-banking-us-postman/actions/workflows/newman.yml)

## Collection
[JSON ⤓](./openbanking-us.postman_collection.json)

## Run the Collection
### Things to Know :point_down:

* A [free Mastercard Developers account](https://developer.mastercard.com/product/open-banking) is required to obtain your **Partner ID**, **Partner Secret** and **App Key**:

![project](https://user-images.githubusercontent.com/3964455/221236073-5661d083-0a04-4d46-9710-3c0c8c9e9a6a.gif)

* Before running the collection, you need a **Customer ID**. For that, follow [Welcome Your First Customer](https://mstr.cd/3Z5de0Q) or run the [setup script](https://github.com/Mastercard/open-banking-us-openapi/blob/main/bin/). This script will call:
  * `addTestingCustomer`
  * `generateConnectUrl` ([Connect Application](https://developer.mastercard.com/open-banking-us/documentation/connect/)). Simply open the URL, search for "FinBank Profiles - A" and add to your test customer all accounts from [`profile_03`](https://developer.mastercard.com/open-banking-us/documentation/test-the-apis/#bank-account-profiles).
  * `refreshCustomerAccounts`

<p align="center">
<img src="https://user-images.githubusercontent.com/3964455/195069664-638aa443-d87d-48ea-94fc-167f2ebfff57.gif" width="300px"/>
</p>

### Import or Fork the Collection

1. Click: [![](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/26779181-8127e4ad-7476-4eca-bf83-f58fba40640e?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D26779181-8127e4ad-7476-4eca-bf83-f58fba40640e%26entityType%3Dcollection%26workspaceId%3D0d6593a8-1921-4fe4-a73c-687c945c5c02#?env%5BTest%20Drive%5D=W3sia2V5IjoicGFydG5lcklkIiwidmFsdWUiOiJ7Y2hhbmdlbWV9IiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQiLCJzZXNzaW9uVmFsdWUiOiJ7Y2hhbmdlbWV9Iiwic2Vzc2lvbkluZGV4IjowfSx7ImtleSI6InBhcnRuZXJTZWNyZXQiLCJ2YWx1ZSI6IntjaGFuZ2VtZX0iLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoic2VjcmV0Iiwic2Vzc2lvblZhbHVlIjoie2NoYW5nZW1lfSIsInNlc3Npb25JbmRleCI6MX0seyJrZXkiOiJhcHBLZXkiLCJ2YWx1ZSI6IntjaGFuZ2VtZX0iLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoic2VjcmV0Iiwic2Vzc2lvblZhbHVlIjoie2NoYW5nZW1lfSIsInNlc3Npb25JbmRleCI6Mn0seyJrZXkiOiJjdXN0b21lcklkIiwidmFsdWUiOiJ7Y2hhbmdlbWV9IiwiZW5hYmxlZCI6dHJ1ZSwic2Vzc2lvblZhbHVlIjoie2NoYW5nZW1lfSIsInNlc3Npb25JbmRleCI6M31d)
2. Select the _Test Drive_ environment (top right) and update `partnerId`, `partnerSecret`, `appKey` and `customerId` variables
3. Click _Send_ on individual requests, or _Run collection_
4. Explore the _Pre-request Script_ and _Tests_ tabs, and update the collection as you wish

### Run the Collection on the Command Line

1. Clone this repository
2. Run `npx newman run openbanking-us.postman_collection.json --env-var partnerId=*** --env-var partnerSecret=*** --env-var appKey=*** --env-var customerId=*** --folder 'All APIs'`

![](https://user-images.githubusercontent.com/3964455/194878975-1b8f3051-68d5-478e-95cb-bd8b15d84379.gif)

### Run the Collection in GitHub

1. [Fork this repository](https://github.com/Mastercard/open-banking-us-postman/fork)
2. Go to _Settings_ > _Secrets_ > _Actions_
3. Create new repository secrets: `PARTNER_ID`, `PARTNER_SECRET` and `APP_KEY`
4. Enable workflows in the _Actions_ tab
5. Click _Run workflow_ under _Newman_. Expected result: :heavy_check_mark:

## What's Next?

* Postman allows you to generate [code snippets](https://learning.postman.com/docs/sending-requests/generate-code-snippets/) you can use into your application
* You may also be interested in generating an API client from the [Open Banking API specification](https://github.com/Mastercard/open-banking-us-openapi)

## Guidelines

The Open Banking Postman Collection was created from the [Open Banking API specification](https://github.com/Mastercard/open-banking-us-openapi) and must be maintained accordingly.
