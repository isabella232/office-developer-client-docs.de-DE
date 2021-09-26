---
title: Kopieren eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4bf3bd7c5d509b0464a620ad0e8a6c00d45b9874
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611000"
---
# <a name="copying-a-profile"></a>Kopieren eines Profils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Möglichkeit zum Erstellen eines Profils besteht darin, aus einem vorhandenen Profil zu kopieren und die erforderlichen Nachrichtendienste und Dienstanbieter zu ändern. Das Kopieren eines Profils umfasst die Verwendung eines Profilverwaltungsobjekts, das von MAPI über die [MAPIAdminProfiles-Funktion](mapiadminprofiles.md) bereitgestellt wird. 
  
 **So kopieren Sie ein Profil**
  
1. Rufen Sie **MAPIAdminProfiles** auf, um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) auf, um auf die Profiltabelle zuzugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des zu kopierenden Profils übereinzugleichen. 
    
4. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile in der Profiltabelle zu suchen. 
    
5. Rufen Sie [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)auf, und übergeben Sie den Wert der **PR_DISPLAY_NAME** Spalte als _lpszOldProfileName-Parameter._ 
    

