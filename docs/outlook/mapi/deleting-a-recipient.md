---
title: Löschen eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791514"
---
# <a name="deleting-a-recipient"></a>Löschen eines Empfängers

  
  
**Betrifft**: Outlook 
  
 **So entfernen einen oder mehrere Einträge im Adressbuch aus einem Container geändert werden**
  
- Rufen Sie die [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode übergeben ein Array von Eintragsbezeichner, die zu löschenden Adressbucheinträge darstellen. **DeleteEntries** kann eine Warnung MAPI_W_PARTIAL_COMPLETION, um anzugeben, dass sie eine oder mehrere Einträge löschen konnte nicht zurückgeben. Für diesen Rückgabewert mit dem Makro **HR_FAILED** testen Sie, und rufen Sie den Container [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, wenn weitere Informationen zu dem Problem benötigt wird. 
    
Wenn Sie einen Zeiger auf einen gelöschten Eintrag [ADRENTRY](adrentry.md) -Struktur in den Cache gespeichert werden, werden Sie dennoch zum Abrufen von Eigenschaften mithilfe des Bezeichners Eintrag sein. Dies ist, da der Eintrag nur zum Löschen markiert ist. MAPI verwaltet eine Zugriffsebene für diese markierte Einträge Verhalten ist erwünscht. 
  

