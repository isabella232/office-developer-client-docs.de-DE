---
title: Verwalten von Profilen und Nachrichtendiensten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 238982026b61f8559560619e6c8dd76db291c9b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564456"
---
# <a name="administering-profiles-and-message-services"></a>Verwalten von Profilen und Nachrichtendiensten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Profil- und Nachrichtendienstverwaltung kann das Erstellen neuer Profile, das Löschen alter Profile und das Ändern des Inhalts vorhandener Profile umfassen, indem die darin enthaltenen Nachrichtendienste und Dienstanbieter geändert werden. Nicht alle Clients unterstützen die Profil- und Nachrichtendienstverwaltung als Standardfeatures. Einige Clients haben nichts weiter mit Profilen zu tun, als ihren Benutzern die Auswahl eines Clients zur Anmeldezeit zu ermöglichen.
  
Wenn Sie die Profil- oder Nachrichtendienstverwaltung unterstützen, verwenden Sie wahrscheinlich die folgenden Schnittstellen, die von mapi implementiert werden:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) zum Verwalten eines Nachrichtendiensts in einem Profil, auf den über [IMAPISession::AdminServices](imapisession-adminservices.md) oder [IProfAdmin::AdminServices](iprofadmin-adminservices.md)zugegriffen werden kann. Messaging-Clients rufen in der Regel **IMAPISession** auf, während Konfigurationsclients oder Clients, die keine Nachrichten senden oder empfangen, **IProfAdmin** aufrufen. Rufen Sie nach Möglichkeit die **IProfAdmin-Methode** auf, da sie nicht dazu führt, dass der Nachrichtendienst gestartet wird. Weitere Informationen zur Verwendung der **IMsgServiceAdmin-Schnittstelle** finden Sie in den folgenden Themen: [Konfigurieren eines Nachrichtendiensts,](configuring-a-message-service.md) [Kopieren eines Nachrichtendiensts](copying-a-message-service.md)und [Löschen eines Nachrichtendiensts.](deleting-a-message-service.md)
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, auf das über die [MAPIAdminProfiles-Funktion](mapiadminprofiles.md) zugegriffen werden kann. Weitere Informationen zur Verwendung der **IProfAdmin-Schnittstelle** finden Sie in den folgenden Themen: [Erstellen eines Profils mithilfe von benutzerdefiniertem Code,](creating-a-profile-by-using-custom-code.md) [Kopieren eines Profils,](copying-a-profile.md) [Löschen eines Profils,](deleting-a-profile.md) [Suchen eines Profilnamens](finding-a-profile-name.md)und [Festlegen eines Standardprofils.](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) zum Verwalten der Eigenschaften in einem Profilabschnitt, auf die über die [IMAPISession::OpenProfileSection-](imapisession-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection-Methode](iprovideradmin-openprofilesection.md) zugegriffen werden kann. Weitere Informationen zu Profilabschnitten finden Sie unter [MAPI-Profile.](mapi-profiles.md)
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) zum Verwalten der Dienstanbieter in einem Nachrichtendienst, auf den über [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)zugegriffen werden kann. Weitere Informationen zur Verwendung der **IProviderAdmin-Schnittstelle** finden Sie unter [Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst.](adding-or-deleting-providers-in-a-message-service.md)
    
Seien Sie vorsichtig bei der Unterstützung der Profil- und Nachrichtendienstverwaltung. Es gibt keine Sicherheitsmaßnahmen zum Schutz vor nachteiligen Änderungen eines verwendeten Profils. MapI kann verhindern, dass Sie ein verwendetes Profil löschen, aber nicht jeden darin enthaltenen Nachrichtendienst löschen. Wenn Sie jeden Nachrichtendienst in einem Profil löschen, werden alle Dienstanbieter in diesen Diensten beendet, wodurch unvorhersehbare Ergebnisse auftreten.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Profils](creating-a-profile.md)
  
> Beschreibt, wie ein Profil erstellt wird.
    
[Kopieren eines Profils](copying-a-profile.md)
  
> Beschreibt, wie ein Profil kopiert wird.
    
[Löschen eines Profils](deleting-a-profile.md)
  
> Beschreibt, wie ein Profil gelöscht wird.
    
[Festlegen eines Standardprofils](setting-a-default-profile.md)
  
> Beschreibt, wie ein Standardprofil festgelegt wird.
    
[Suchen eines Profilnamens](finding-a-profile-name.md)
  
> Beschreibt, wie ein Name eines Profils gefunden wird.
    
[Hinzufügen eines Nachrichtendiensts](adding-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst hinzugefügt wird.
    
[Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst konfiguriert wird.
    
[Kopieren eines Nachrichtendiensts](copying-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst in ein Profil kopiert wird.
    
[Löschen eines Nachrichtendiensts](deleting-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst gelöscht wird.
    
[Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md)
  
> Beschreibt, wie Anbieter in einem Nachrichtendienst hinzugefügt oder gelöscht werden.
    

