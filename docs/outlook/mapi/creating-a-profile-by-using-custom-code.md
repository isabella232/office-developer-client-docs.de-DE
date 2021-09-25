---
title: Erstellen eines Profils mithilfe von benutzerdefiniertem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f2990c2bacd40ac1f98a658d278e444d73495ff9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551779"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Erstellen eines Profils mithilfe von benutzerdefiniertem Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie Code zum Erstellen eines Profils schreiben möchten, stellen Sie sicher, dass Sie wissen, wie Profileinträge und der Typ und die Menge der für jeden Eintrag benötigten Informationen sortiert werden. Die Auswirkungen der Sortierung von Einträgen in einem Profil werden in [MAPI-Profilen](mapi-profiles.md)erläutert.
  
 **So erstellen Sie ein Profil mit C- oder C++-Code**
  
1. Lesen Sie die Headerdatei für jeden Nachrichtendienst. Verstehen Sie, welche Eigenschaften Sie konfigurieren müssen und welche Werte Sie verwenden werden.
    
2. Rufen Sie die [MAPIAdminProfiles-Funktion](mapiadminprofiles.md) auf, um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
3. Rufen Sie [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) auf, um Ihr Profil zu erstellen. Wenn Sie ein Profil mit den Nachrichtendiensten erstellen möchten, die im Abschnitt **[Standarddienste]** von MAPISVC aufgeführt sind. Legen Sie in der INF-Datei das MAPI_DEFAULT_SERVICE Flag fest. Wenn Sie dem Benutzer die Eingabe von Konfigurationsinformationen ermöglichen möchten, legen Sie das flag MAPI_DIALOG fest. Stellen Sie sicher, dass Sie dieses Kennzeichen festlegen, wenn nicht alle erforderlichen Informationen über MAPISVC verfügbar sind. INF-Datei. **CreateProfile** ruft die Einstiegspunktfunktion für jeden Nachrichtendienst auf, der dem Profil hinzugefügt werden soll, wobei MSG_SERVICE_CREATE als  _ulContext-Parameter_ festgelegt wird. 
    
4. Rufen [Sie IProfAdmin::AdminServices](iprofadmin-adminservices.md) auf, um ein Nachrichtendienst-Verwaltungsobjekt abzurufen. 
    
5. Verwenden Sie das Nachrichtendienst-Verwaltungsobjekt, um dem Profil Nachrichtendienste hinzuzufügen. Für jeden Nachrichtendienst, den Sie hinzufügen möchten:
    
1. Rufen Sie die [IMsgServiceAdmin::CreateMsgService-Methode](imsgserviceadmin-createmsgservice.md) auf, um den neuen Nachrichtendienst zu erstellen. 
    
2. Rufen Sie [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf, und übergeben Sie die **MAPIUID-Struktur** des soeben erstellten Diensts und ein Eigenschaftenwertarray mit den zugehörigen Konfigurationseigenschaften. 
    
6. Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um den Bezeichner eines neu hinzugefügten Diensts abzurufen, der die **eigenschaft PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) ist, um auf die Nachrichtendiensttabelle zuzugreifen und nach der Zeile zu suchen, die den Nachrichtendienst darstellt. Die letzte Zeile in der Tabelle stellt den zuletzt hinzugefügten Nachrichtendienst dar. 
    
Rufen Sie zum Temporären eines neuen Profils die [IProfAdmin::D eleteProfile-Methode](iprofadmin-deleteprofile.md) unmittelbar nach der Anmeldung auf. **DeleteProfile** markiert das neue Profil als gelöscht, während es für die Dauer der Sitzung verwendet werden kann. Da sie nicht in der Profiltabelle der Sitzung enthalten ist, können andere Clients sie nicht verwenden. 
  

