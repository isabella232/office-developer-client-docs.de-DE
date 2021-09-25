---
title: Festlegen eines Standardprofils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c7c28bcab989c778e98da6619bba6f8c628f7553
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586733"
---
# <a name="setting-a-default-profile"></a>Festlegen eines Standardprofils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Standardprofil ist das Profil, das verwendet wird, wenn Sie im Aufruf von [MAPILogonEx](mapilogonex.md)nicht explizit ein Profil angeben und stattdessen das MAPI_USE_DEFAULT-Flag festlegen.
  
 **So richten Sie ein Standardprofil ein**
  
1. Rufen Sie die [MAPIAdminProfiles-Funktion](mapiadminprofiles.md) auf, um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
2. Rufen [Sie IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)auf. **SetDefaultProfile** legt die **eigenschaft PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) für das neue Standardprofil fest und entfernt die Einstellung für das vorherige Standardprofil.
    

