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
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591772"
---
# <a name="setting-a-default-profile"></a>Festlegen eines Standardprofils

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Das Standardprofil ist das Profil, das verwendet wird, wenn Sie nicht explizit eine im Aufruf [MAPILogonEx](mapilogonex.md), stattdessen das MAPI_USE_DEFAULT-Flag festlegen angeben.
  
 **Ein Standardprofil herstellen**
  
1. Rufen Sie die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers. 
    
2. Rufen Sie [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** die **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))-Eigenschaft für neues Standardprofil festgelegt und die Einstellung für das vorherige Standardprofil entfernt.
    

