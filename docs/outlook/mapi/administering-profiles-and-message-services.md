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
  
Die Profil- und Nachrichtendienstverwaltung kann das Erstellen neuer Profile, das Löschen alter Profile und das Ändern der Inhalte vorhandener Profile umfassen, indem die darin enthaltenen Nachrichtendienste und Dienstanbieter geändert werden. Nicht alle Clients unterstützen die Profil- und Nachrichtendienstverwaltung als Standardfeatures. Einige Clients haben nichts weiter mit Profilen zu tun, als ihren Benutzern die Auswahl eines zur Anmeldezeit zu ermöglichen.
  
Wenn Sie die Profil- oder Nachrichtendienstverwaltung unterstützen, verwenden Sie wahrscheinlich die folgenden Schnittstellen, die von MAPI implementiert werden:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) zum Verwalten eines Nachrichtendiensts in einem Profil, auf das über [IMAPISession::AdminServices](imapisession-adminservices.md) oder [IProfAdmin::AdminServices](iprofadmin-adminservices.md)zugegriffen werden kann. Messagingclients rufen in der Regel **IMAPISession auf,** während Konfigurationsclients oder Clients, die keine Nachrichten senden oder empfangen, **IProfAdmin aufrufen.** Rufen Sie nach Möglichkeit die **IProfAdmin-Methode** auf, da dadurch der Nachrichtendienst nicht gestartet wird. Weitere Informationen zur Verwendung der **IMsgServiceAdmin-Schnittstelle** finden Sie in den folgenden [Themen:](configuring-a-message-service.md)Konfigurieren eines Nachrichtendiensts, [](copying-a-message-service.md)Kopieren eines Nachrichtendiensts und Löschen eines [Nachrichtendiensts.](deleting-a-message-service.md)
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, auf das über die [MAPIAdminProfiles-Funktion zugegriffen werden](mapiadminprofiles.md) kann. Weitere Informationen zur Verwendung der **IProfAdmin-Schnittstelle** finden Sie in den folgenden Themen: Erstellen eines Profils mithilfe von benutzerdefiniertem [Code,](creating-a-profile-by-using-custom-code.md)Kopieren eines [Profils,](copying-a-profile.md)Löschen eines Profils, [](deleting-a-profile.md)Suchen eines Profilnamens [und](finding-a-profile-name.md)Festlegen eines Standardprofils. [](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) zum Verwalten der Eigenschaften in einem Profilabschnitt, auf den über die [IMAPISession::OpenProfileSection-](imapisession-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection-Methode](iprovideradmin-openprofilesection.md) zugegriffen werden kann. Weitere Informationen zu Profilabschnitten finden Sie unter [MAPI Profiles](mapi-profiles.md).
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) zum Verwalten der Dienstanbieter in einem Nachrichtendienst, auf den über [IMsgServiceAdmin::AdminProviders zugegriffen werden kann.](imsgserviceadmin-adminproviders.md) Weitere Informationen zur Verwendung der **IProviderAdmin-Schnittstelle** finden Sie unter Hinzufügen oder Löschen von Anbietern [in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md).
    
Seien Sie vorsichtig bei der Unterstützung der Profil- und Nachrichtendienstverwaltung. Es gibt keine Schutzmaßnahmen zum Schutz vor einer negativen Änderung eines verwendeten Profils. MAPI kann verhindern, dass Sie ein verwendetes Profil löschen, aber Nicht verhindern, dass Sie alle Nachrichtendienste löschen. Wenn Sie jeden Nachrichtendienst in einem Profil löschen, werden alle Dienstanbieter in diesen Diensten beendet, wodurch unvorhersehbare Ergebnisse auftreten.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Profils](creating-a-profile.md)
  
> Beschreibt das Erstellen eines Profils.
    
[Kopieren eines Profils](copying-a-profile.md)
  
> Beschreibt das Kopieren eines Profils.
    
[Löschen eines Profils](deleting-a-profile.md)
  
> Beschreibt das Löschen eines Profils.
    
[Festlegen eines Standardprofils](setting-a-default-profile.md)
  
> Beschreibt das Festlegen eines Standardprofils.
    
[Suchen eines Profilnamens](finding-a-profile-name.md)
  
> Beschreibt, wie Sie einen Namen eines Profils finden.
    
[Hinzufügen eines Nachrichtendiensts](adding-a-message-service.md)
  
> Beschreibt das Hinzufügen eines Nachrichtendiensts.
    
[Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md)
  
> Beschreibt das Konfigurieren eines Nachrichtendiensts.
    
[Kopieren eines Nachrichtendiensts](copying-a-message-service.md)
  
> Beschreibt, wie ein Nachrichtendienst in ein Profil kopiert wird.
    
[Löschen eines Nachrichtendiensts](deleting-a-message-service.md)
  
> Beschreibt das Löschen eines Nachrichtendiensts.
    
[Hinzufügen oder Löschen von Anbietern in einem Nachrichtendienst](adding-or-deleting-providers-in-a-message-service.md)
  
> Beschreibt, wie Anbieter in einem Nachrichtendienst hinzugefügt oder gelöscht werden.
    

