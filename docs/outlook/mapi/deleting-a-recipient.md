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
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421046"
---
# <a name="deleting-a-recipient"></a>Löschen eines Empfängers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So entfernen Sie Adressbucheinträge aus einem änderbaren Container**
  
- Rufen Sie die [IABContainer::D eleteentries](iabcontainer-deleteentries.md) -Methode auf, und übergeben Sie ein Array von Eintrags Bezeichnern, die die zu löschenden Adressbucheinträge darstellen. **DeleteEntries** kann eine Warnung zurückgeben, MAPI_W_PARTIAL_COMPLETION, um anzugeben, dass ein oder mehrere Einträge nicht gelöscht werden konnten. Testen Sie diesen Rückgabewert mit dem **HR_FAILED** -Makro, und rufen Sie die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode des Containers auf, wenn weitere Informationen zum Problem erforderlich sind. 
    
Wenn Sie einen Zeiger auf die [Miet](adrentry.md) Struktur eines gelöschten Eintrags in Ihrem Cache speichern, können Sie die Eigenschaften weiterhin mithilfe des Eintrags Bezeichners abrufen. Der Grund ist, dass der Eintrag nur zum Löschen markiert ist. MAPI verwaltet eine Ebene des Zugriffs auf diese markierten Einträge nach Design. 
  

