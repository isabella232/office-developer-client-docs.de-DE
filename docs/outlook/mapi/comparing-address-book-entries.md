---
title: Vergleichen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415355"
---
# <a name="comparing-address-book-entries"></a>Vergleichen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABLogon::CompareEntryIDs-Implementierung](iablogon-compareentryids.md) Ihres Anbieters vergleicht die Eintragsbezeichner für zwei Objekte Ihres Anbieters. MAPI ruft diese Methode auf, nachdem sie ermittelt haben, dass die beiden Eintragsbezeichner die registrierte [MAPIUID Ihres Anbieters enthalten.](mapiuid.md) Daher muss die **CompareEntryIDs-Methode** nicht überprüfen, ob die eintragsbezeichner, die für die  _Parameter lpEntryID1_ und  _lpEntryID2_ übergeben werden, zu Ihrem Anbieter gehören. 
  
Das **Aufrufen von IABLogon::CompareEntryIDs** entspricht dem Abrufen der **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft für jedes der beiden Objekte und dem direkten Vergleich.
  
 **So implementieren Sie CompareEntryIds**
  
1. Überprüfen Sie den Typ der übergebenen Eintragsbezeichner, wenn der Anbieter diese Informationen speichert. Beispielsweise kann eine Eintrags-ID zu einem Messagingbenutzer gehören, während der andere zu einer Verteilerliste gehört. Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie zurück. 
    
2. Vergleichen Sie die Größen der beiden Eintragsbezeichner. Wenn sie nicht identisch sind, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie zurück. 
    
3. Überprüfen Sie, ob die Größe der Eintragsbezeichner die richtige Größe für ihren Typ ist. Wenn nicht, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE ein, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID. 
    
4. Überprüfen Sie, ob die Eintragsbezeichner identisch sind. Wenn sie gleich vergleichen, legen Sie den Inhalt des  _lpulResult-Parameters_ auf TRUE und zurückgeben. Legen Sie andernfalls den Wert auf FALSE, bevor Sie ihn zurückgeben. 
    
5. Wenn Ihr Anbieter einen kurzfristigen Eintragsbezeichner mit einem langfristigen Bezeichner vergleicht, sollte er den gleichen Vergleich haben.
    

