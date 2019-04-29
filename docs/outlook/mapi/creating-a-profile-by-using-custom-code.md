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
  
Wenn Sie Code zum Erstellen eines Profils schreiben, stellen Sie sicher, dass Sie wissen, wie Sie Profileinträge und die Art und Menge der Informationen, die für jeden Eintrag benötigt werden, bestellen können. Die Auswirkungen der Reihenfolge von Einträgen in einem Profil werden in [MAPI](mapi-profiles.md)-Profilen erläutert.
  
 **So erstellen Sie ein Profil mit C-oder C++-Code**
  
1. Lesen Sie die Headerdatei für jeden Nachrichtendienst. Verstehen Sie, welche Eigenschaften Sie konfigurieren müssen und welche Werte Sie verwenden werden.
    
2. Rufen Sie die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion auf, um einen **IProfAdmin** -Schnittstellenzeiger abzurufen. 
    
3. Rufen Sie [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) auf, um Ihr Profil zu erstellen. Wenn Sie ein Profil mit den Nachrichtendiensten erstellen möchten, die im Abschnitt **[Default Services]** des Mapisvc aufgeführt sind. INF-Datei, legen Sie das MAPI_DEFAULT_SERVICE-Flag fest. Wenn Sie möchten, dass der Benutzerkonfigurationsinformationen eingeben kann, legen Sie das MAPI_DIALOG-Flag fest. Stellen Sie sicher, dass Sie dieses Flag festlegen, wenn nicht alle erforderlichen Informationen über die MAPISVC verfügbar sind. INF-Datei. **CreateProfile** Ruft die Einstiegspunktfunktion für jeden Nachrichtendienst auf, der dem Profil hinzugefügt werden soll, wobei MSG_SERVICE_CREATE als _ulContext_ -Parameter festgelegt ist. 
    
4. Rufen Sie [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) auf, um ein Nachrichtendienst-Verwaltungsobjekt abzurufen. 
    
5. Verwenden Sie das Nachrichtendienst-Verwaltungsobjekt, um dem Profilnachrichten Dienste hinzuzufügen. Für jeden Nachrichtendienst, den Sie hinzufügen möchten:
    
1. Rufen Sie die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode auf, um den neuen Nachrichtendienst zu erstellen. 
    
2. Rufen Sie [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)auf, und übergeben Sie die **MAPIUID** -Struktur des soeben erstellten Diensts und ein Eigenschaftenwert Array mit den Konfigurationseigenschaften. 
    
6. Zum Abrufen des Bezeichners eines neu hinzugefügten Diensts, bei dem es sich um die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft handelt, rufen Sie [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) auf, um auf die Nachrichtendienst Tabelle zuzugreifen und nach der Zeile zu suchen, die der Nachrichtendienst. Die letzte Zeile in der Tabelle stellt den zuletzt hinzugefügten Nachrichtendienst dar. 
    
Wenn Sie ein neues Profil als temporär festlegen möchten, rufen Sie die [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) -Methode unmittelbar nach der Anmeldung auf. **DeleteProfile** markiert das neue Profil als gelöscht, während es für die Dauer der Sitzung nutzbar gemacht wird. Da es nicht in der Profiltabelle der Sitzung enthalten ist, können andere Clients es nicht verwenden. 
  

