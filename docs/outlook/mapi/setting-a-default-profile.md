---
title: Festlegen eines Standardprofils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795503"
---
# <a name="setting-a-default-profile"></a>Festlegen eines Standardprofils

  
  
**Betrifft**: Outlook 
  
Das Standardprofil ist das Profil, das verwendet wird, wenn Sie nicht explizit eine im Aufruf [MAPILogonEx](mapilogonex.md), stattdessen das MAPI_USE_DEFAULT-Flag festlegen angeben.
  
 **Ein Standardprofil herstellen**
  
1. Rufen Sie die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers. 
    
2. Rufen Sie [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** die **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))-Eigenschaft für neues Standardprofil festgelegt und die Einstellung für das vorherige Standardprofil entfernt.
    

