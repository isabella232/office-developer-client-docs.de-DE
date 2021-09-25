---
title: Vergleichen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1a4a06a76ec9bb7d46de9d13d42cfca00c2c353b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571997"
---
# <a name="comparing-address-book-entries"></a>Vergleichen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABLogon::CompareEntryIDs-Implementierung](iablogon-compareentryids.md) Ihres Anbieters vergleicht die Eintragsbezeichner für zwei Objekte des Anbieters. MAPI ruft diese Methode auf, nachdem festgestellt wurde, dass die beiden Eintragsbezeichner die registrierte [MAPIUID](mapiuid.md)Ihres Anbieters enthalten. Daher muss die **CompareEntryIDs-Methode** nicht überprüfen, ob die Eintragsbezeichner, die für die Parameter  _lpEntryID1_ und  _lpEntryID2_ übergeben wurden, zu Ihrem Anbieter gehören. 
  
Das Aufrufen von **IABLogon::CompareEntryIDs** entspricht dem Abrufen der **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) -Eigenschaft für jedes der beiden Objekte und dem direkten Vergleich dieser Objekte.
  
 **So implementieren Sie CompareEntryIds**
  
1. Überprüfen Sie den Typ der übergebenen Eintragsbezeichner, wenn ihr Anbieter diese Informationen speichert. Beispielsweise kann ein Eintragsbezeichner zu einem Messagingbenutzer gehören, während der andere zu einer Verteilerliste gehört. Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE fest und geben sie zurück. 
    
2. Vergleichen Sie die Größen der beiden Eintragsbezeichner. Wenn sie nicht identisch sind, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE fest und geben sie zurück. 
    
3. Überprüfen Sie, ob die Größe der Eintragsbezeichner die richtige Größe für ihren Typ ist. Wenn nicht, legen Sie den Inhalt des  _lpulResult-Parameters_ auf FALSE fest, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID zurück. 
    
4. Überprüfen Sie, ob die Eintragsbezeichner identisch sind. Wenn sie gleich verglichen werden, legen Sie den Inhalt des  _lpulResult-Parameters_ auf TRUE fest und geben sie zurück. Andernfalls legen Sie ihn vor der Rückgabe auf FALSE fest. 
    
5. Wenn Ihr Anbieter einen kurzfristigen Eintragsbezeichner mit einem langfristigen Bezeichner vergleicht, sollte dieser gleich verglichen werden.
    

