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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335532"
---
# <a name="comparing-address-book-entries"></a>Vergleichen von Adressbucheinträgen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) -Implementierung des Anbieters vergleicht die Eintrags-IDs für zwei Objekte des Anbieters. MAPI ruft diese Methode auf, nachdem festgestellt wurde, dass die beiden Eintragsbezeichner die registrierte [MAPIUID](mapiuid.md)Ihres Anbieters enthalten. Daher muss Ihre **CompareEntryIDs** -Methode nicht überprüfen, ob die Eintrags-IDs, die für die Parameter _lpEntryID1_ und _lpEntryID2_ übergeben wurden, zu Ihrem Anbieter gehören. 
  
Das Aufrufen von **IABLogon:: CompareEntryIDs** entspricht dem Abrufen der **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md))-Eigenschaft für jedes der beiden Objekte und dem direkten Vergleich.
  
 **So implementieren Sie CompareEntryIds**
  
1. Überprüfen Sie den Typ der Eintrags-IDs, die übergeben werden, wenn Ihr Anbieter diese Informationen speichert. Beispielsweise kann ein Eintragsbezeichner zu einem Messagingbenutzer gehören, während der andere zu einer Verteilerliste gehören kann. Wenn die Typen nicht übereinstimmen, legen Sie den Inhalt des _lpulResult_ -Parameters auf false und Return zurück. 
    
2. Vergleichen Sie die Größen der beiden Eintragsbezeichner. Wenn Sie nicht identisch sind, legen Sie den Inhalt des _lpulResult_ -Parameters auf false und Return zurück. 
    
3. Stellen Sie sicher, dass die Größe der Eintragsbezeichner die richtige Größe für Ihren Typ ist. Wenn dies nicht der Fall ist, legen Sie den Inhalt des _lpulResult_ -Parameters auf false fest, und geben Sie den Fehlerwert MAPI_E_UNKNOWN_ENTRYID. 
    
4. Überprüfen Sie, ob die Eintragsbezeichner identisch sind. Wenn Sie gleichmäßig vergleichen, legen Sie den Inhalt des _lpulResult_ -Parameters auf true fest, und geben Sie zurück. Andernfalls legen Sie ihn auf FALSE fest, bevor Sie zurückkehren. 
    
5. Wenn Ihr Anbieter eine kurzfristige Eintrags-ID mit einem langfristigen Bezeichner vergleicht, sollten Sie gleichmäßig vergleichen.
    

