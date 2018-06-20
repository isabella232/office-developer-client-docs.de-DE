---
title: Abrufen von Empfängereigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795385"
---
# <a name="retrieving-recipient-properties"></a>Abrufen von Empfängereigenschaften
  
**Betrifft**: Outlook 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Zugriff auf eine oder mehrere Eigenschaften eines Adresseintrags Adressbuch
  
1. Rufen Sie für jeden Eintrag Address Book von Interesse [IAddrBook::OpenEntry](iaddrbook-openentry.md), übergeben die Eintrags-ID des Ziels messaging-Benutzer- oder Verteilerliste aus.
    
2. Klicken Sie dann einen der folgenden Schritte aus:
    
   - Rufen Sie für jeden Eintrag Adressbuch Adresse von Interesse, mit der eine oder mehrere Eigenschaften zum Abrufen einer Liste der messaging-Benutzer oder die Verteilerliste [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode. 
    
   - Rufen Sie [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), übergeben eine [ADRLIST](adrlist.md) -Struktur, die alle Eigenschaften für alle gewünschten Adressbucheinträge enthält. Da durch Aufrufen von **PrepareRecips** Informationen für mehrere Adresse Adressbucheinträge zurückgeben kann, ist die Strategie vorzuziehen, wenn Sie mehrere Empfänger interessiert sind. 
    

