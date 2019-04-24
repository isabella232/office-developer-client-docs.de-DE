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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285230"
---
# <a name="copying-a-profile"></a>Kopieren eines Profils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Möglichkeit zum Erstellen eines Profils besteht darin, aus einem vorhandenen Profil zu kopieren und die erforderlichen Nachrichtendienste und Dienstanbieter zu ändern. Zum Kopieren eines Profils muss ein Profilverwaltungsobjekt verwendet werden, das von MAPI über die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion bereitgestellt wird. 
  
 **So kopieren Sie ein Profil**
  
1. Rufen Sie **MAPIAdminProfiles** auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen. 
    
2. Aufrufen von [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable für den Zugriff auf die Profiltabelle. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen des zu kopierenden Profils entspricht. 
    
4. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile in der Profiltabelle zu suchen. 
    
5. Rufen Sie [IProfAdmin:: CopyProfile](iprofadmin-copyprofile.md)auf, und übergeben Sie den Wert der **PR_DISPLAY_NAME** -Spalte als _lpszOldProfileName_ -Parameter. 
    

