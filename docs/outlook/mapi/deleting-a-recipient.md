---
title: Löschen eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582945"
---
# <a name="deleting-a-recipient"></a>Löschen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So entfernen einen oder mehrere Einträge im Adressbuch aus einem Container geändert werden**
  
- Rufen Sie die [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode übergeben ein Array von Eintragsbezeichner, die zu löschenden Adressbucheinträge darstellen. **DeleteEntries** kann eine Warnung MAPI_W_PARTIAL_COMPLETION, um anzugeben, dass sie eine oder mehrere Einträge löschen konnte nicht zurückgeben. Für diesen Rückgabewert mit dem Makro **HR_FAILED** testen Sie, und rufen Sie den Container [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, wenn weitere Informationen zu dem Problem benötigt wird. 
    
Wenn Sie einen Zeiger auf einen gelöschten Eintrag [ADRENTRY](adrentry.md) -Struktur in den Cache gespeichert werden, werden Sie dennoch zum Abrufen von Eigenschaften mithilfe des Bezeichners Eintrag sein. Dies ist, da der Eintrag nur zum Löschen markiert ist. MAPI verwaltet eine Zugriffsebene für diese markierte Einträge Verhalten ist erwünscht. 
  

