---
title: Verwalten von Benutzerprofilen und Message-Dienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791270"
---
# <a name="administering-profiles-and-message-services"></a>Verwalten von Benutzerprofilen und Message-Dienste

  
  
**Betrifft**: Outlook 
  
Benutzerprofil und Nachricht, dass Verwalten des Diensts umfassen kann, neue Profile erstellen, alte Profile löschen und Ändern des Inhalts der vorhandene Profile durch Ändern der Message-Dienste und die darin enthaltenen Dienstanbieter. Nicht alle Clients unterstützen Benutzerprofil und Nachricht Verwalten des Diensts als Standardfeatures. Einige Clients müssen keine weiteren Schritte durchgeführt mit Profilen, die als ihre Benutzer bei der Anmeldung auswählen können.
  
Verwalten des Diensts Profil oder einer Nachricht unterstützen, sind wahrscheinlich, dass Sie die folgenden Schnittstellen verwenden möchten, die von MAPI implementiert werden:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) eine Message Service in einem Profil, das über [IMAPISession::AdminServices](imapisession-adminservices.md) oder [IProfAdmin::AdminServices](iprofadmin-adminservices.md)verwalten. Messaging-Clients rufen **IMAPISession** normalerweise während der Konfiguration oder Clients, die nicht senden oder Empfangen von Nachrichten, **IProfAdmin**aufrufen. Wenn möglich, rufen Sie die **IProfAdmin** -Methode, da sie nicht den Dienst gestartet werden führt. Weitere Informationen zur Verwendung der **IMsgServiceAdmin** -Schnittstelle finden Sie unter den folgenden Themen: [Konfigurieren einer Nachricht](configuring-a-message-service.md), [eine Message Service kopieren](copying-a-message-service.md)und [Löschen einer Nachricht-Dienstes](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) zum Verwalten eines Profils, über die Funktion ["MAPIAdminProfiles"](mapiadminprofiles.md) zugegriffen werden. Weitere Informationen zur Verwendung der **IProfAdmin** -Schnittstelle finden Sie unter den folgenden Themen: [Erstellen eines Profils durch Verwendung benutzerdefinierter Code](creating-a-profile-by-using-custom-code.md), [Kopieren eines Profils](copying-a-profile.md), [Löschen ein Profil](deleting-a-profile.md), [Suchen Sie einen Profilnamen](finding-a-profile-name.md)und [Einstellung ein Standardprofil](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) zur Aufrechterhaltung der Eigenschaften in einem Profilabschnitt kann über die [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode zugegriffen werden. Weitere Informationen über Profil Abschnitte finden Sie unter [MAPI-Profile](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) zur Verwaltung der Dienstanbieter in einem Message-Dienst über [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)zugegriffen werden. Weitere Informationen zur Verwendung der **IProviderAdmin** -Schnittstelle finden Sie unter [Hinzufügen oder Löschen von Anbietern in einem Message-Dienst](adding-or-deleting-providers-in-a-message-service.md).
    
Achten Sie darauf, dass in Ihre Unterstützung von Profil- und Nachricht verwalten. Es gibt keine Sicherheitsfunktionen zum Schutz gegen ändern sich negativ auf ein Profil, das verwendet wird. MAPI kann verhindern, dass Sie löschen ein Profil verwendet, aber kann nicht verhindern, dass Sie alle Messagingdiensts darin löschen. Wenn Sie jeden Nachrichtendienst in einem Profil löschen, hält alle-Dienstanbieter in dieser Dienste und verursacht dadurch zu unvorhersehbaren Ergebnissen eintritt.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Profils](creating-a-profile.md)
  
> Beschreibt, wie Sie ein Profil erstellen.
    
[Kopieren eines Profils](copying-a-profile.md)
  
> Beschreibt, wie ein Profil zu kopieren.
    
[Löschen eines Profils](deleting-a-profile.md)
  
> Beschreibt, wie ein Profil zu löschen.
    
[Ein Standardprofil festlegen](setting-a-default-profile.md)
  
> Beschreibt, wie ein Standardprofil festgelegt.
    
[Suchen einen Profilnamen](finding-a-profile-name.md)
  
> Beschreibt, wie ein Profil einen Namen zu suchen.
    
[Hinzufügen eines Dienstes Nachricht](adding-a-message-service.md)
  
> Beschreibt, wie einen Nachrichtendienst hinzufügen.
    
[Konfigurieren einer Nachricht](configuring-a-message-service.md)
  
> Beschreibt, wie eine Message Service konfigurieren.
    
[Kopieren eines Nachricht-Diensts](copying-a-message-service.md)
  
> Beschreibt, wie eine Messagingdiensts zu einem Profil zu kopieren.
    
[Löschen einer Nachricht-Dienstes](deleting-a-message-service.md)
  
> Beschreibt, wie eine Messagingdiensts zu löschen.
    
[Hinzufügen oder Löschen von Anbietern in einem Message-Dienst](adding-or-deleting-providers-in-a-message-service.md)
  
> Beschreibt das Hinzufügen oder Löschen von Anbietern in einem Message-Dienst.
    

