---
title: Löschen eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 39ad9792fce6c282725f40073bf103b0afb4aee6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584626"
---
# <a name="deleting-a-recipient"></a>Löschen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So entfernen Sie einen oder mehrere Adressbucheinträge aus einem modifizierbaren Container**
  
- Rufen Sie die [IABContainer::D eleteEntries-Methode auf,](iabcontainer-deleteentries.md) und übergeben Sie ein Array von Eintragsbezeichnern, die die zu löschenden Adressbucheinträge darstellen. **DeleteEntries** kann eine Warnung MAPI_W_PARTIAL_COMPLETION zurückgeben, um anzugeben, dass mindestens einer der Einträge nicht gelöscht werden konnte. Testen Sie diesen Rückgabewert mit dem **HR_FAILED-Makro,** und rufen Sie die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Containers auf, wenn weitere Informationen zu dem Problem erforderlich sind. 
    
Wenn Sie einen Zeiger auf die [ADRENTRY-Struktur](adrentry.md) eines gelöschten Eintrags im Cache halten, können Sie weiterhin Eigenschaften mithilfe des Eintragsbezeichners abrufen. Dies liegt daran, dass der Eintrag nur zum Löschen markiert ist. Die MAPI verwaltet entwurfsbedingt eine Zugriffsebene auf diese markierten Einträge. 
  

