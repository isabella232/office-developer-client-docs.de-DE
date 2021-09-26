---
title: Abrufen von Empfängereigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ecf340bcf63048ad8d29ba411aa3553e4890bf78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599116"
---
# <a name="retrieving-recipient-properties"></a>Abrufen von Empfängereigenschaften
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>So greifen Sie auf eine oder mehrere Eigenschaften eines Adressbucheintrags zu
  
1. Rufen Sie für jeden interessanten Adressbucheintrag [IAddrBook::OpenEntry](iaddrbook-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Zielnachrichtenbenutzers oder der Verteilerliste.
    
2. Führen Sie dann eine der folgenden Aktionen aus:
    
   - Rufen Sie die [IMAPIPropProp::GetProps-Methode](imapiprop-getprops.md) des Messagingbenutzers oder der Verteilerliste für jeden gewünschten Adressbucheintrag mit einer Liste der abzurufenden Eigenschaften auf. 
    
   - Rufen Sie [IAddrBook::P repareRecips auf](iaddrbook-preparerecips.md)und übergeben Sie eine [ADRLIST-Struktur,](adrlist.md) die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält. Da ein Aufruf von **PrepareRecips** Informationen für mehrere Adressbucheinträge zurückgeben kann, ist dies die bevorzugte Strategie, wenn Sie an mehreren Empfängern interessiert sind. 
    

