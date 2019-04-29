---
title: Suchen nach einem Profilnamen
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
# <a name="finding-a-profile-name"></a>Suchen nach einem Profilnamen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients müssen manchmal den Namen des Profils ermitteln, das derzeit für die Sitzung verwendet wird, den Namen des Standardprofils oder den Namen eines alternativen Profils, das auf dem Computer installiert ist.
  
Es gibt verschiedene Möglichkeiten, den Namen eines Profils während einer Sitzung abzurufen. Wenn Sie den Namen eines Profils suchen müssen, das nicht unbedingt derjenige ist, der für die Sitzung verwendet wird, verwenden Sie das erste Verfahren. Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie die zweite Vorgehensweise. Wenn Sie den Namen des aktuellen Profils für die Sitzung suchen müssen, verwenden Sie das letzte Verfahren. 
  
 **So suchen Sie nach dem Namen eines beliebigen Profils**
  
1. Rufen Sie [MAPIAdminProfiles](mapiadminprofiles.md) auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen. 
    
2. Aufrufen von [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable für den Zugriff auf die Profiltabelle. 
    
3. Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode der Profiltabelle auf, um alle Zeilen in der Tabelle abzurufen und zu überprüfen, ob Sie das Zielprofil darstellt. 
    
 **So suchen Sie nach dem Namen des Standardprofils**
  
1. Rufen Sie [MAPIAdminProfiles](mapiadminprofiles.md)auf.
    
2. Aufrufen von [IProfAdmin::](iprofadmin-getprofiletable.md) getprofilable für den Zugriff auf die Profiltabelle. 
    
3. Erstellen Sie eine Eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, um **PR_DEFAULT_PROFILE** ([PIDTAGDEFAULTPROFILE (](pidtagdefaultprofile-canonical-property.md)) mit dem Wert true zu vergleichen.
    
4. Rufen Sie [IMAPITable:: FindRow](imapitable-findrow.md) auf, um die Zeile in der Profiltabelle zu suchen, die das Standardprofil darstellt. Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Spalte enthält den Namen des Standardprofils.
    
 **So suchen Sie nach dem Namen des aktuellen Profils**
  
Führen Sie einen der folgenden Schritte aus, um den Namen des aktuellen Profils zu ermitteln:
  
- Wenn Sie die [MAPIUID](mapiuid.md) -Struktur haben, die einen der Abschnitte des aktuellen Profils darstellt, übergeben Sie diese im Parameter _lpUID_ an [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md). Rufen Sie die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft des Profil Abschnitts mithilfe der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode ab. 
    
- Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen und die Zeile zu finden, deren **PR_RESOURCE_TYPE** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md)) auf MAPI_SUBSYSTEM festgelegt ist. Die **PR_DISPLAY_NAME** -Spalte für diese Zeile ist der Profil Name. Verwenden Sie die Status-Tabelle nicht während des Starts, da Sie eine Anwendung blockiert, bis der MAPI-Spooler alle Transportanbieter initialisiert hat. Dies kann Ihre Leistung beeinträchtigen. 
    

