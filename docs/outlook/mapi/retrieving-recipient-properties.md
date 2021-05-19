---
title: Abrufen von Empfängereigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426674"
---
# <a name="retrieving-recipient-properties"></a>Abrufen von Empfängereigenschaften
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>So greifen Sie auf eine oder mehrere Eigenschaften eines Adressbucheintrags zu
  
1. Rufen Sie für jeden adressbucheintrag von Interesse [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie die Eintrags-ID des Zielnachrichtenbenutzers oder der Verteilerliste.
    
2. Gehen Sie dann wie folgt vor:
    
   - Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Messagingbenutzers oder der Verteilerliste für jeden interessierten Adressbucheintrag mit einer Liste der abzurufenden Eigenschaften auf. 
    
   - Rufen [Sie IAddrBook::P repareRecips](iaddrbook-preparerecips.md)auf, und übergeben Sie eine [ADRLIST-Struktur,](adrlist.md) die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält. Da ein Aufruf **von PrepareRecips** Informationen für mehrere Adressbucheinträge zurückgeben kann, ist dies die bevorzugte Strategie, wenn Sie an mehreren Empfängern interessiert sind. 
    

