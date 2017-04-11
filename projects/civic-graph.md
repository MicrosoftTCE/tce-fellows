## Namecheap

The domain name civicgraph.io is registered with Namecheap. The DNS records are currently managed in Azure; the correct Azure name servers should be specified in Namecheap and shouldn't need to be updated unless the Azure DNS zone changes.

## GitHub

We keep code in GitHub, because it's free, easy, and what the civic tech community prefers.
All code lives under the MicrosoftTCE organization, except anything that we want to keep private, which lives directly under the microsoftny user (because this user is grandfathered into a $7/month plan for private repos).

## Azure Deployment

The microsoftny user is an admin of the MicrosoftTCE org so that its credentials can be used to deploy to Azure. Do not modify this user's role, or deployments might break (alternatively, create a deployment-specific account).

## New developers

New developers should user their existing GitHub account. It should have 2FA enabled (please enable if this is not already the case).

# Azure

## Entity hierarchy

Account owner: civic-machine@outlook.com
 * Directory / Tenant: civicmachineoutlook (civicmachineoutlook.onmicrosoft.com)
 * Tenant ID: 163c1d45-04ce-4368-89cf-96531765fbb7
 
## Subscriptions
 * d6b238db-2ea5-4c4b-8a39-401d161baddf (Sponsorship)
 * e434c18f-dd55-41c1-b741-1581ee3df62c (Pay-As-You-Go)
 * 28b96368-d0e1-4ff0-ba75-3fd32ad8525b (Pay-As-You-Go)
 * Suspended due to PastDue (converted from Sponsorship offer to Pay-as-you-go after #58531 was cancelled)

## Tools

The Azure CLI will be helpful to have.
You'll also probably want [Visual Studio Code](https://aka.ms/devicelogin)
 and the Azure Resource Manager Tools extension as described in this article.

## Subscriptions

A subscription is a method of payment for Azure resources. Ideally, we (TCE) should have a single sponsorship subscription; we currently have multiple, as we're in a state of transition. 
Once a sponsorship subscription reaches the end of its life, it automatically converts to a Pay-as-you-go subscription, at which point charges begin accruing on the credit card specified with the subscription. To avoid this, a new sponsorship subscription should be requested at that time.

## Identity & Authentication Management (IAM)

civic-machine@outlook.com is the account owner (and owner of subscriptions), so it's basically a root/God/administrator account. For the sake of an audit trail and not sharing credentials, we should never use this account to access the Azure portal.
Instead, the easiest way of managing IAM will be to add TCE members as subscription owners. Each owner of a subscription will have full access to all resources within that subscription.
This can—of course—be more fine-grained (e.g. on a per-project or per-application basis, if there's a desire to restrict certain Azure resources to certain users).
Subscription owners are managed by:
1.	Browsing to the Subscriptions blade (ensure you're using the correct directory)
2.	Selecting a subscription
3.	Selecting the "Access control (IAM)" blade
4.	Adding the desired user

## Regions

When creating a Resource Group, be conscious of which region is used. Pick a region that has all the desired services for needed by the Resource Group.

## Ross notes

Look into: Resource Group --> Automation Script --> 

Update civic-graph-UI repo README w/ deployment instructions

Performance tests
Python Application Insights

## Civic Graph

## Civic Graph UI

Pricing tier: S1 Standard
 * Mostly for the 5 slots (staging environments)
 * We don't care about auto-scale since this is static and the CDN will take care of that

There are a few options for how to serve the static Civic Graph UI. Here's the thought process we went through:
 * Serve from Azure Web App (static) — this is what we currently do
 * Bummer: must commit build code
 * But also kind of a feature – extra step, but flexibility
 * Gives us 5 slots (using the S1 pricing tier) for staging environments
 * Plays pretty nicely with CDN, SSL, etc.
 * Serve from Azure Web App using Continuous Integration
 * This would be nice (allow the build step to happen on Azure, so we don't need to commit build code), but currently the CI beta only works for ASP apps
 * Serve from GitHub Pages, put an Azure CDN in front of it for metrics and SSL
 * Not bad, but has a production dependency on GH Pages being up
 * Also doesn't allow for multiple concurrent environments (prod-only)
 * Doesn't solve the build step problem (would need to push build to its own branch or convert the whole thing to a Jekyll site)


## API

Per: https://www.kennethreitz.org/essays/a-better-pip-workflow
 * pip install -r requirements-to-freeze.txt --upgrade
 * pip freeze > requirements.txt





