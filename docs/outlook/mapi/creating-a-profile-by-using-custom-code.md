---
title: Erstellen eines Profils mithilfe von benutzerdefiniertem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413304"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Erstellen eines Profils mithilfe von benutzerdefiniertem Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie Code zum Erstellen eines Profils schreiben möchten, stellen Sie sicher, dass Sie wissen, wie Sie Profileinträge und den Typ und die Menge der Informationen, die für jeden Eintrag erforderlich sind, bestellen. Die Auswirkungen der Sortierung von Einträgen in einem Profil werden in [MAPI Profiles erläutert.](mapi-profiles.md)
  
 **So erstellen Sie ein Profil mit C- oder C++-Code**
  
1. Lesen Sie die Headerdatei für jeden Nachrichtendienst. Verstehen Sie, welche Eigenschaften Sie konfigurieren müssen und welche Werte Sie verwenden.
    
2. Rufen Sie die [MAPIAdminProfiles-Funktion](mapiadminprofiles.md) auf, um einen **IProfAdmin-Schnittstellenzeiger** abzurufen. 
    
3. Rufen [Sie IProfAdmin::CreateProfile auf,](iprofadmin-createprofile.md) um Ihr Profil zu erstellen. Wenn Sie ein Profil mit den Nachrichtendiensten erstellen möchten, die im **Abschnitt [Standarddienste]** des MAPISVC aufgeführt sind. INF-Datei, legen Sie das MAPI_DEFAULT_SERVICE. Wenn Sie dem Benutzer die Eingabe von Konfigurationsinformationen ermöglichen möchten, legen Sie das MAPI_DIALOG. Stellen Sie sicher, dass Sie dieses Flag festlegen, wenn nicht alle erforderlichen Informationen über MAPISVC verfügbar sind. INF-Datei. **CreateProfile** ruft die Einstiegspunktfunktion für jeden Nachrichtendienst auf, der dem Profil hinzugefügt werden soll, MSG_SERVICE_CREATE als  _ulContext-Parameter_ festgelegt ist. 
    
4. Rufen [Sie IProfAdmin::AdminServices auf,](iprofadmin-adminservices.md) um ein Nachrichtendienstverwaltungsobjekt zu erhalten. 
    
5. Verwenden Sie das Nachrichtendienstverwaltungsobjekt, um dem Profil Nachrichtendienste hinzuzufügen. Für jeden Nachrichtendienst, den Sie hinzufügen möchten:
    
1. Rufen Sie [die IMsgServiceAdmin::CreateMsgService-Methode](imsgserviceadmin-createmsgservice.md) auf, um den neuen Nachrichtendienst zu erstellen. 
    
2. Rufen [Sie IMsgServiceAdmin::ConfigureMsgService auf,](imsgserviceadmin-configuremsgservice.md)übergeben Sie die **MAPIUID-Struktur** des gerade erstellten Diensts und ein Eigenschaftenwertarray mit seinen Konfigurationseigenschaften. 
    
6. Rufen Sie [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um den Bezeichner eines neu hinzugefügten Diensts abzurufen, bei dem es sich um die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft handelt, um auf die Nachrichtendiensttabelle zu zugreifen und nach der Zeile zu suchen, die den Nachrichtendienst darstellt. Die letzte Zeile in der Tabelle stellt den zuletzt hinzugefügten Nachrichtendienst dar. 
    
Um ein neues Profil temporär zu machen, rufen Sie die [IProfAdmin::D eleteProfile-Methode](iprofadmin-deleteprofile.md) unmittelbar nach der Anmeldung auf. **DeleteProfile** wird das neue Profil als gelöscht markieren, während es für die Dauer der Sitzung verwendet werden kann. Da sie nicht in der Profiltabelle der Sitzung enthalten ist, können andere Clients sie nicht verwenden. 
  

