---
title: Erstellen eines Profils mithilfe von benutzerdefiniertem Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74869293215b86c69ab4e0b1337be6014419fa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791488"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Erstellen eines Profils mithilfe von benutzerdefiniertem Code

  
  
**Betrifft**: Outlook 
  
Wenn Sie dem Schreiben von Code zum Erstellen eines Profils auswählen, stellen Sie sicher, dass Sie verstehen, wie bestellen profileinträgen und den Typ und die Menge der Informationen, die für jeden Eintrag erforderlich ist. Die Auswirkungen der Einträge in einem Profil Sortierung in [MAPI-Profile](mapi-profiles.md)erläutert wird.
  
 **Zum Erstellen eines Profils mit C oder C++-code**
  
1. Lesen Sie die Headerdatei für jeden Nachrichtendienst. Verstehen, welche Eigenschaften, die Sie konfigurieren müssen und welche Werte verwenden.
    
2. Rufen Sie die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers. 
    
3. Rufen Sie [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) um Ihr Profil zu erstellen. Wenn Sie ein Profil mit der Nachrichtendienste aufgeführt, in der die Datei MAPISVC im Abschnitt **[Default Services]** erstellen möchten. INF-Datei, legen Sie das MAPI_DEFAULT_SERVICE-Flag. Wenn Sie den Benutzer zur Eingabe von Konfigurationsinformationen aktivieren möchten, legen Sie die MAPI_DIALOG-Flag. Stellen Sie sicher, dass Sie dieses Flag festlegen, wenn nicht alle erforderlichen Informationen über die Datei MAPISVC verfügbar ist. INF-Datei. **CreateProfile** Ruft die Funktion Eintrag für jeden Nachrichtendienst mit MSG_SERVICE_CREATE als _UlContext_ -Parameter festgelegt, das Profil hinzugefügt werden soll. 
    
4. Rufen Sie [IProfAdmin::AdminServices](iprofadmin-adminservices.md) , um eine Nachricht Service Administration-Objekt zu erhalten. 
    
5. Verwenden Sie das Objekt "Message" Service Administration Message-Dienste zu dem Profil hinzufügen. Für jeden Nachrichtendienst, die Sie hinzufügen möchten:
    
1. Rufen Sie die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode, um den neuen Dienst erstellen. 
    
2. Rufen Sie [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), übergeben Sie die **MAPIUID** Struktur des Diensts, den Sie gerade erstellt haben und ein Array-Eigenschaft Wert Konfiguration Eigenschaften. 
    
6. Rufen Sie auf, um den Bezeichner für den Dienst neu hinzugefügte abzurufen, das die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft ist, [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) Zugriff auf die Nachricht Service Tabelle und suchen Sie nach der Zeile, die darstellt der Nachrichtendienst. Die letzte Zeile in der Tabelle wird die zuletzt hinzugefügten Messagingdiensts darstellen. 
    
Um ein neues Profil temporäre machen, rufen Sie die [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) -Methode unmittelbar nach der Anmeldung. **DeleteProfile** kennzeichnet das neue Profil als gelöscht und dass es für die Dauer der Sitzung verwendet werden kann. Weil es nicht in der Sitzung Profiltabelle enthalten, werden andere Clients nicht verwenden. 
  

