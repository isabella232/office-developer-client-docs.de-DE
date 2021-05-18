---
title: Suchen eines Profilnamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407921"
---
# <a name="finding-a-profile-name"></a>Suchen eines Profilnamens

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen manchmal den Namen des Profils finden, das derzeit für die Sitzung verwendet wird, den Namen des Standardprofils oder den Namen eines alternativen Profils, das auf dem Computer installiert ist.
  
Es gibt mehrere Möglichkeiten, den Namen eines Profils während einer Sitzung abzurufen. Wenn Sie den Namen eines Profils suchen müssen, das nicht unbedingt für die Sitzung verwendet wird, verwenden Sie das erste Verfahren. Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie das zweite Verfahren. Wenn Sie den Namen des aktuellen Profils für die Sitzung suchen müssen, verwenden Sie das letzte Verfahren. 
  
 **So suchen Sie den Namen eines profils**
  
1. Rufen [Sie MAPIAdminProfiles auf,](mapiadminprofiles.md) um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
2. Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen. 
    
3. Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) der Profiltabelle auf, um alle Zeilen in der Tabelle abzurufen und die einzelnen Zeilen zu untersuchen, um festzustellen, ob sie Ihr Zielprofil darstellt. 
    
 **So suchen Sie den Namen des Standardprofils**
  
1. Rufen [Sie MAPIAdminProfiles auf.](mapiadminprofiles.md)
    
2. Rufen [Sie IProfAdmin::GetProfileTable auf,](iprofadmin-getprofiletable.md) um auf die Profiltabelle zu zugreifen. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit [einer SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) mit dem Wert TRUE zu entsprechen.
    
4. Rufen [Sie IMAPITable::FindRow](imapitable-findrow.md) auf, um die Zeile in der Profiltabelle zu finden, die das Standardprofil darstellt. Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enthält den Namen des Standardprofils.
    
 **So suchen Sie den Namen des aktuellen Profils**
  
Führen Sie einen der folgenden Schritte aus, um den Namen des aktuellen Profils zu finden:
  
- Wenn Sie die [MAPIUID-Struktur](mapiuid.md) haben, die einen der Abschnitte des aktuellen Profils darstellt, übergeben Sie sie im  _lpUID-Parameter_ an [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Rufen Sie die PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft des Profilabschnitts mithilfe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) ab. 
    
- Rufen [Sie IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zu zugreifen und die Zeile zu suchen, für die **die Spalte PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) auf MAPI_SUBSYSTEM. Die **PR_DISPLAY_NAME** spalte für diese Zeile ist der Profilname. Verwenden Sie die Statustabelle beim Starten nicht, da sie eine Anwendung blockiert, bis der MAPI-Spooler alle Transportanbieter initialisiert hat. Dies kann ihre Leistung beeinträchtigen. 
    

