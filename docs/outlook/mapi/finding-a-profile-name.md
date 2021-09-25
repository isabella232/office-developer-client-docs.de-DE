---
title: Suchen eines Profilnamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8278d0ed8e3f695fc0c516f54c24540ea3c7babb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588049"
---
# <a name="finding-a-profile-name"></a>Suchen eines Profilnamens

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen manchmal den Namen des Profils suchen, das derzeit für die Sitzung verwendet wird, den Namen des Standardprofils oder den Namen eines alternativen Profils, das auf dem Computer installiert ist.
  
Es gibt einige Möglichkeiten, den Namen eines Profils während einer Sitzung abzurufen. Wenn Sie den Namen eines Profils suchen müssen, das nicht notwendigerweise der name ist, der für die Sitzung verwendet wird, verwenden Sie die erste Prozedur. Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie die zweite Prozedur. Wenn Sie den Namen des aktuellen Profils für die Sitzung suchen müssen, verwenden Sie das letzte Verfahren. 
  
 **So suchen Sie den Namen eines beliebigen Profils**
  
1. Rufen Sie [MAPIAdminProfiles](mapiadminprofiles.md) auf, um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) auf, um auf die Profiltabelle zuzugreifen. 
    
3. Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Profiltabelle auf, um alle Zeilen in der Tabelle abzurufen, und untersuchen Sie jede Zeile, um zu ermitteln, ob sie Ihr Zielprofil darstellt. 
    
 **So suchen Sie den Namen des Standardprofils**
  
1. Rufen Sie [MAPIAdminProfiles auf.](mapiadminprofiles.md)
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) auf, um auf die Profiltabelle zuzugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) mit dem Wert TRUE übereinzuordnen.
    
4. Rufen Sie [IMAPITable::FindRow](imapitable-findrow.md) auf, um die Zeile in der Profiltabelle zu suchen, die das Standardprofil darstellt. Die **Spalte PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enthält den Namen des Standardprofils.
    
 **So suchen Sie den Namen des aktuellen Profils**
  
Führen Sie einen der folgenden Schritte aus, um den Namen des aktuellen Profils zu finden:
  
- Wenn Sie über die [MAPIUID-Struktur](mapiuid.md) verfügen, die einen der Abschnitte des aktuellen Profils darstellt, übergeben Sie sie im  _LpUID-Parameter_ an [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Rufen Sie die **eigenschaft PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) des Profilabschnitts mithilfe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) ab. 
    
- Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen und die Zeile zu suchen, deren **spalte PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) auf MAPI_SUBSYSTEM festgelegt ist. Die **PR_DISPLAY_NAME** Spalte für diese Zeile ist der Profilname. Verwenden Sie die Statustabelle während des Startvorgangs nicht, da sie eine Anwendung blockiert, bis der MAPI-Spooler die Initialisierung aller Transportanbieter abgeschlossen hat. Dies kann die Leistung beeinträchtigen. 
    

