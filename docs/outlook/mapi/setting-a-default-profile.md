---
title: Festlegen eines Standardprofils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439814"
---
# <a name="setting-a-default-profile"></a>Festlegen eines Standardprofils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Standardprofil ist das Profil, das verwendet wird, wenn Sie im Aufruf von [MAPILogonEx](mapilogonex.md)nicht explizit angeben, sondern stattdessen das MAPI_USE_DEFAULT-Flag festlegen.
  
 **So richten Sie ein Standardprofil ein**
  
1. Rufen Sie die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen. 
    
2. Rufen Sie [IProfAdmin:: SetDefaultProfile](iprofadmin-setdefaultprofile.md)auf. **SetDefaultProfile** legt die **PR_DEFAULT_PROFILE** ([pidtagdefaultprofile (](pidtagdefaultprofile-canonical-property.md))-Eigenschaft für das neue Standardprofil fest und entfernt die Einstellung für das vorherige Standardprofil.
    

