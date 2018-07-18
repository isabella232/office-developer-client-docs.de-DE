---
title: Vergleichen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791420"
---
# <a name="comparing-address-book-entries"></a>Vergleichen von Adressbucheinträgen

  
  
**Betrifft**: Outlook 
  
Der Implementierung des Anbieters [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) vergleicht den Eintrag-IDs für zwei Objekte des Anbieters. MAPI ruft diese Methode auf, nachdem festgestellt wurde, dass die zwei-Eintragsbezeichner des Anbieters enthalten [MAPIUID](mapiuid.md)registriert. Aus diesem Grund muss **CompareEntryIDs** -Methode nicht überprüfen, ob die für die Parameter _lpEntryID1_ und _lpEntryID2_ übergebenen Eintragsbezeichner an Ihren Anbieter gehören. 
  
Aufrufen von **IABLogon::CompareEntryIDs** entspricht dem die **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft für jedes der beiden Objekte abrufen und diese direkt vergleicht.
  
 **CompareEntryIds implementieren**
  
1. Überprüfen Sie den Typ der Eintragsbezeichner übergeben, wenn vom Dienstanbieter, die betreffenden Informationen gespeichert werden. Beispielsweise kann eine Eintrags-ID zu einem messaging Benutzer gehören, während der anderen in einer Verteilerliste gehören möglicherweise. Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des Parameters _LpulResult_ auf false festgelegt und zurückgegeben. 
    
2. Vergleichen Sie die Größen der zwei Eintrags-IDs. Wenn sie nicht identisch sind, legen Sie den Inhalt des Parameters _LpulResult_ auf FALSE und zurück. 
    
3. Überprüfen Sie, dass die Größe der Eintragsbezeichner die richtige Größe für ihren Typ ist. Wenn dies nicht der Fall ist, legen Sie den Inhalt des Parameters _LpulResult_ auf false fest, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID zurück. 
    
4. Überprüfen Sie, ob die Eintragsbezeichner identisch sind. Wenn sie gleichermaßen vergleichen, den Inhalt des Parameters _LpulResult_ auf TRUE festgelegt und zurückgegeben. Andernfalls ihn auf FALSE festgelegt vor der Rückgabe. 
    
5. Wenn der Anbieter eine kurzfristige Eintrags-ID mit einem langfristige Bezeichner verglichen wird ist, sollte sie gleichermaßen vergleichen.
    

