---
title: MDES Pre-Digitization
---

# Overview

The Mastercard Digital Enablement Service (MDES) is a suite of on-behalf-of (OBO) services that supports the management and generation of digital payment tokens to enable simpler and secure digital payment experiences. MDES was developed to facilitate the transition from consumer account credentials (PAN) to digital credentials (tokens). These digital credentials maybe:

*   provisioned to mobile devices, enabling consumers to perform payments via existing contactless point-of-sale (POS) systems, or via remote payment use cases such as in-app payments.
*   stored on file by merchants and digital Wallet Providers (WP), allowing them to exchange payment cards on file with digital payment tokens.  
      
    

The MDES Pre-Digitization service is a set of processes that must happen to convert these credentials into tokens and before a token is ready for use. It is available in two flavors:

*   [ISO Network Messages](https://techdocs.mastercard.com/bundle/m_CI/page/ezo1655306963779.html) - Issuers must configure the network messages in the Message Profile using the MDES Manager application during on-boarding process.
*   [Web services (API)](https://developer.mastercard.com/mdes-pre-digitization/documentation/api-basics/) - Issuers participating in MDES must implement the web services provided by the Digitization Service in MDES.  
    

# Key Benefits

*   Low development effort in transitioning to digital payments.
*   Reduced time to market.
*   Support for Digital Service Providers where third-party processors lack support for digital payments.
*   Reduced implementation costs and maintenance of network message infrastructure.

# How it Works

The web services are used to inform Issuers of MDES services being requested by, or on-behalf of, their account holders. Issuers may provide information in their responses to guide or inform the Account holder’s experience through the Wallet Provider.

The following diagram illustrates integration of the MDES Pre-Digitization API with an Issuer web service complying with the API described in this document:

![](https://static.developer.mastercard.com/content/mdes-pre-digitization/documentation/img/predig_overview.png)

## Web Services Implementation

![](https://static.developer.mastercard.com/content/mdes-pre-digitization/documentation/img/web_services_implementation.png)

This diagram illustrates a web service managed by the Issuer or Service Provider that implements pre-digitization services using the MDES Pre-Digitization API. This includes:

*   Authorizing the creation of a token (digitization) or activation of a service.
*   Authenticating the Account holder, managing the Activation Methods list and the Activation Code Distribution Methods.

## Hybrid Implementation

![](https://static.developer.mastercard.com/content/mdes-pre-digitization/documentation/img/hybrid_implementation.png)

This diagram shows a hybrid implementation of the pre-digitization services where:

*   The Issuer uses the Tokenization Authorization pre-digitization network message for authorizing the creation of a token (digitization).
*   The Issuer designates a Web Service (e.g. managed by a Service Provider) implementing the MDES Pre-Digitization API for authentication of the Account holder, managing both the Activation Methods list and the Activation Code Distribution Methods.

For more information about MDES Pre-Digitization, please read the following use cases:

*   [Token Requestor Initiated Tokenization](https://developer.mastercard.com/mdes-pre-digitization/documentation/use_case/tokenization/)
    
*   [Issuer Initiated Tokenization](https://developer.mastercard.com/mdes-pre-digitization/documentation/use_case/issuer-tokenization/)
