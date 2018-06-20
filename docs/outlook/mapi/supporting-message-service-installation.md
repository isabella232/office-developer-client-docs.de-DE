---
title: Unterstützende Nachricht Service-Installation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795668"
---
# <a name="supporting-message-service-installation"></a>Unterstützende Nachricht Service-Installation

  
  
**Betrifft**: Outlook 
  
Das Setup-Programm für die Installation von Ihrer Messagingdiensts sollten folgendermaßen vorgehen:
  
1. Kopieren Sie Service Nachrichtendateien, wie die Messagingdiensts und Service Provider-DLLs, von einer CD oder Diskette, einem lokalen Laufwerk auf der Arbeitsstation. Die Dateien, die kopiert werden müssen, abhängig von Ihrer Messagingdiensts ab. Kopieren Sie in der Regel mindestens eine DLL-Datei.
    
2. Die Datei "Mapisvc.inf" Konfiguration Einträge hinzugefügt. Weitere Informationen zum Ändern der Datei, um die-Dienstanbieter in Ihrer Messagingdiensts zu unterstützen finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Fügen Sie Einträge, je nach der Registrierung des Systems für die Message-Dienste. Weitere Informationen dazu, wie die Einträge in der Registrierung angezeigt werden soll finden Sie unter [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md).
    
4. Erstellen Sie ein Standardprofil aus, wenn eine noch nicht vorhanden ist mit einer der folgenden Elemente:
    
  - Der Profil-Assistent zum Erstellen eines Profils mithilfe der Benutzerinteraktion durch eine Reihe von Dialogfeldern. Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Erstellen eines Profils mithilfe der Profil-Assistent](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion. Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als die-Profil-Assistent zum Konfigurieren der Nachrichtendienste und Festlegen von Profileigenschaften. 
    
Platzieren Sie das Setup-Programm in einem öffentlichen Verzeichnis. Dies ist wichtig, da die meisten Konfiguration Clients wie beispielsweise die Systemsteuerung erfordert, dass Benutzer auf den Namen des Verzeichnisses eingeben. Die Systemsteuerung Ruft ein Setup-Programm aus, wenn ein Benutzer klickt auf die Schaltfläche **Hinzufügen** , das Dialogfeld **Datenträger ruft** und den Pfad zu dem Programm gibt. Der Systemsteuerung das Programm ausgeführt wird und Ihre Messagingdiensts Eintrag Point-Funktion aufruft, mit dem _UlContext_ -Parameter auf MSG_SERVICE_INSTALL festgelegt. 
  
> [!CAUTION]
> Da Profile einer geeigneten Bestandteil der MAPI-Architektur sind, werden Sie sicher, dass das Installationsprogramm nicht alles im Standardprofil speichert, die zum erneuten Erstellen schwierig wäre. Es gibt keine Dienstprogramme für die Benutzerprofildienst-Wiederherstellung, zum Verschieben von Profilen von einem Computer an eine andere, für Offline-Sicherung oder für einzelne oder globale Wiederherstellung von Sicherungskopien. 
  
## <a name="see-also"></a>Siehe auch



[Nachricht Service-Implementierung](message-service-implementation.md)

