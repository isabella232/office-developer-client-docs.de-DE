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
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564934"
---
# <a name="copying-a-profile"></a>Kopieren eines Profils

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Möglichkeit zum Erstellen eines Profils ist Kopieren eines vorhandenen Profils und ändern Sie die erforderlichen Message-Dienste und -Dienstanbieter. Kopieren eines Profils beinhaltet die Verwendung einer Profile Administration-Objekt von MAPI über die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) bereitgestellt. 
  
 **Kopieren ein Profils**
  
1. Rufen Sie **"MAPIAdminProfiles"** zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers. 
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle. 
    
3. Erstellen Sie eine eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) Struktur entsprechend **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des Profils, kopiert werden soll. 
    
4. Rufen Sie [IMAPITable](imapitable-findrow.md) , um die entsprechende Zeile in der Profiltabelle zu suchen. 
    
5. Rufen Sie [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), der Wert der Spalte **PR_DISPLAY_NAME** als _LpszOldProfileName_ -Parameter übergeben. 
    

