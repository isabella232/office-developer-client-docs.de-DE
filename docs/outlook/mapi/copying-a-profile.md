---
title: Kopieren eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424728"
---
# <a name="copying-a-profile"></a>Kopieren eines Profils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Möglichkeit zum Erstellen eines Profils ist das Kopieren aus einem vorhandenen Profil und das Ändern der erforderlichen Nachrichtendienste und Dienstanbieter. Das Kopieren eines Profils umfasst die Verwendung eines Profilverwaltungsobjekts, das von MAPI über die [MAPIAdminProfiles-Funktion bereitgestellt](mapiadminprofiles.md) wird. 
  
 **So kopieren Sie ein Profil**
  
1. Rufen **Sie MAPIAdminProfiles auf,** um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
2. Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit [einer SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des zu kopierenden Profils zu übereinstimmen. 
    
4. Rufen [Sie IMAPITable::FindRow auf,](imapitable-findrow.md) um die entsprechende Zeile in der Profiltabelle zu finden. 
    
5. Rufen [Sie IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)auf, und übergeben Sie den Wert der **PR_DISPLAY_NAME** als _lpszOldProfileName-Parameter._ 
    

