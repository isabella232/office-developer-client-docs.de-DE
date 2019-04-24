---
title: Unterstützen der Nachrichtendienst Installation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350631"
---
# <a name="supporting-message-service-installation"></a>Unterstützen der Nachrichtendienst Installation

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Setupprogramm für die Installation des Nachrichtendiensts sollte folgendermaßen vorgehen:
  
1. Kopieren Sie Nachrichtendienst Dateien wie den Nachrichtendienst und die Dienstanbieter-DLLs von einer CD oder einem Datenträger auf ein lokales Laufwerk auf der Arbeitsstation. Die zu kopierenden Dateien hängen vom Nachrichtendienst ab. In der Regel kopieren Sie mindestens eine DLL.
    
2. Fügen Sie der Konfigurationsdatei MAPISVC. inf Einträge hinzu. Weitere Informationen zum Ändern dieser Datei zur Unterstützung der Dienstanbieter im Nachrichtendienst finden Sie unter [Datei Format von MapiSvc. inf](file-format-of-mapisvc-inf.md).
    
3. Fügen Sie der Systemregistrierung für Nachrichtendienste entsprechende Einträge hinzu. Weitere Informationen dazu, wie die Einträge in der Systemregistrierung angezeigt werden sollen, finden Sie unter [Installieren des MAPI-Subsystems](installing-the-mapi-subsystem.md).
    
4. Erstellen Sie ein Standardprofil, wenn es noch nicht vorhanden ist, indem Sie eines der folgenden Elemente verwenden:
    
  - Der Profil-Assistent zum Erstellen eines Profils mithilfe von Benutzerinteraktionen über eine Reihe von Dialogfeldern. Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion. Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als der Profil-Assistent zum Konfigurieren der Nachrichtendienste und zum Festlegen von Profileigenschaften. 
    
Platzieren Sie das Setupprogramm in einem bestimmten öffentlichen Verzeichnis. Dies ist wichtig, da bei den meisten Konfigurations Clients wie der Systemsteuerung Benutzer den Namen des Verzeichnisses eingeben müssen. Die Systemsteuerung Ruft ein Setupprogramm auf, wenn ein Benutzer auf die Schaltfläche **Hinzufügen** klickt, das Dialogfeld **Datenträger** aufruft und den Pfad zum Programm angibt. Die Systemsteuerung führt das Programm aus und ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_INSTALL festgelegt ist. 
  
> [!CAUTION]
> Da Profile ein entbehrlicher Teil der MAPI-Architektur sind, müssen Sie sicherstellen, dass das Installationsprogramm nichts im Standardprofil speichert, das nur schwer neu erstellt werden kann. Es gibt keine Dienstprogramme für die Profil Wiederherstellung, um Profile von einem Computer auf einen anderen zu übertragen, für die Offlinesicherung oder für die individuelle oder globale Wiederherstellung von Sicherungskopien. 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtendienst Implementierung](message-service-implementation.md)

