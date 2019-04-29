---
title: Verwalten von Profilen und Nachrichtendiensten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410560"
---
# <a name="administering-profiles-and-message-services"></a>Verwalten von Profilen und Nachrichtendiensten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Verwaltung von Profil-und Nachrichtendiensten kann dazu dienen, neue Profile zu erstellen, alte Profile zu löschen und die Inhalte vorhandener Profile zu ändern, indem Sie die darin enthaltenen Nachrichtendienste und Dienstanbieter ändern. Nicht alle Clients unterstützen die Verwaltung von Profil-und Nachrichtendiensten als Standardfunktionen. Einige Clients haben nichts mehr mit Profilen zu tun, als es Ihren Benutzern bei der Anmeldung zu erlauben, eine auszuwählen.
  
Wenn Sie die Verwaltung des Profil-oder Nachrichtendiensts unterstützen, können Sie die folgenden Schnittstellen verwenden, die von MAPI implementiert werden:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) zum Verwalten eines Nachrichtendiensts in einem Profil, auf das entweder über [IMAPISession:: AdminServices](imapisession-adminservices.md) oder [IProfAdmin:: AdminServices](iprofadmin-adminservices.md)zugegriffen werden kann. Messaging-Clients rufen in der Regel **IMAPISession** auf, während Konfigurations Clients oder Clients, die keine Nachrichten senden oder empfangen, **IProfAdmin**aufrufen. Rufen Sie nach Möglichkeit die **IProfAdmin** -Methode auf, da der Nachrichtendienst nicht gestartet wird. Weitere Informationen zur Verwendung der **IMsgServiceAdmin** -Schnittstelle finden Sie in den folgenden Themen: [Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md), [Kopieren eines Nachrichten](copying-a-message-service.md)Diensts und [Löschen eines Nachrichtendiensts](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, auf das über die [MAPIAdminProfiles](mapiadminprofiles.md) -Funktion zugegriffen werden kann. Weitere Informationen zur Verwendung der **IProfAdmin** -Schnittstelle finden Sie in den folgenden Themen: [Erstellen eines Profils mithilfe von benutzerdefiniertem Code](creating-a-profile-by-using-custom-code.md), [Kopieren eines Profils](copying-a-profile.md), [Löschen eines](deleting-a-profile.md)Profils, [Suchen eines Profilnamens](finding-a-profile-name.md)und [Festlegen eines Standardprofil](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) zum Verwalten der Eigenschaften in einem Profil Abschnitt, auf die über die [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) -oder [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode zugegriffen werden kann. Weitere Informationen zu Profil Abschnitten finden Sie unter [MAPI-Profile](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) zum Verwalten der Dienstanbieter in einem Nachrichtendienst, auf die über [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md)zugegriffen werden kann. Weitere Informationen zur Verwendung der **IProviderAdmin** -Schnittstelle finden Sie unter [Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md).
    
Achten Sie auf die Unterstützung der Verwaltung von Profil-und Nachrichtendiensten. Es gibt keine Schutzvorkehrungen, die gegen eine nachteilige Änderung eines verwendeten Profils geschützt werden müssen. MAPI kann das Löschen eines verwendeten Profils verhindern, kann jedoch nicht verhindern, dass Sie jeden Nachrichtendienst darin löschen. Wenn Sie jeden Nachrichtendienst in einem Profil löschen, werden alle Dienstanbieter in diesen Diensten angehalten, wodurch unvorhersehbare Ergebnisse auftreten.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Profils](creating-a-profile.md)
  
> Beschreibt das Erstellen eines Profils.
    
[Kopieren eines Profils](copying-a-profile.md)
  
> Beschreibt das Kopieren eines Profils.
    
[Löschen eines Profils](deleting-a-profile.md)
  
> Beschreibt das Löschen eines Profils.
    
[Festlegen eines Standardprofils](setting-a-default-profile.md)
  
> Beschreibt, wie ein Standardprofil festgelegt wird.
    
[Suchen nach einem Profilnamen](finding-a-profile-name.md)
  
> Beschreibt, wie Sie einen Namen eines Profils finden.
    
[Hinzufügen eines Nachrichtendiensts](adding-a-message-service.md)
  
> Beschreibt das Hinzufügen eines Nachrichtendiensts.
    
[Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst konfiguriert wird.
    
[Kopieren eines Nachrichtendiensts](copying-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst in ein Profil kopiert wird.
    
[Löschen eines Nachrichtendiensts](deleting-a-message-service.md)
  
> Beschreibt das Löschen eines Nachrichtendiensts.
    
[Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md)
  
> Beschreibt das Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst.
    

