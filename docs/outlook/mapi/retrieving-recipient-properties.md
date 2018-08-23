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
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585437"
---
# <a name="retrieving-recipient-properties"></a>Abrufen von Empfängereigenschaften
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Zugriff auf eine oder mehrere Eigenschaften eines Adresseintrags Adressbuch
  
1. Rufen Sie für jeden Eintrag Address Book von Interesse [IAddrBook::OpenEntry](iaddrbook-openentry.md), übergeben die Eintrags-ID des Ziels messaging-Benutzer- oder Verteilerliste aus.
    
2. Klicken Sie dann einen der folgenden Schritte aus:
    
   - Rufen Sie für jeden Eintrag Adressbuch Adresse von Interesse, mit der eine oder mehrere Eigenschaften zum Abrufen einer Liste der messaging-Benutzer oder die Verteilerliste [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode. 
    
   - Rufen Sie [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), übergeben eine [ADRLIST](adrlist.md) -Struktur, die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält. Da durch Aufrufen von **PrepareRecips** Informationen für mehrere Adresse Adressbucheinträge zurückgeben kann, ist die Strategie vorzuziehen, wenn Sie mehrere Empfänger interessiert sind. 
    

