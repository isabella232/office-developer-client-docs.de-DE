---
title: Unterstützung der Nachrichtendienstinstallation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 963c786a7b8dd426c9986241fa7cbda3387ac2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566353"
---
# <a name="supporting-message-service-installation"></a>Unterstützung der Nachrichtendienstinstallation

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Setupprogramm für die Installation Des Nachrichtendiensts sollte folgendermaßen vorgehen:
  
1. Kopieren Sie Nachrichtendienstdateien, z. B. nachrichtendienst- und dienstanbieter-DLLs, von einer CD oder einem Datenträger auf ein lokales Laufwerk auf der Arbeitsstation. Welche Dateien kopiert werden müssen, hängt von Ihrem Nachrichtendienst ab. In der Regel kopieren Sie mindestens eine DLL.
    
2. Fügen Sie der Konfigurationsdatei Mapisvc.inf Einträge hinzu. Weitere Informationen zum Ändern dieser Datei zur Unterstützung der Dienstanbieter in Ihrem Nachrichtendienst finden Sie unter [Dateiformat von MapiSvc.inf.](file-format-of-mapisvc-inf.md)
    
3. Fügen Sie der Systemregistrierung für Nachrichtendienste gegebenenfalls Einträge hinzu. Weitere Informationen dazu, wie die Einträge in der Systemregistrierung angezeigt werden sollen, finden Sie unter [Installieren des MAPI-Subsystems.](installing-the-mapi-subsystem.md)
    
4. Erstellen Sie ein Standardprofil, wenn eines noch nicht vorhanden ist, indem Sie eines der folgenden Elemente verwenden:
    
  - Der Profil-Assistent zum Erstellen eines Profils mithilfe von Benutzerinteraktionen über eine Reihe von Dialogfeldern. Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Erstellen eines Profils mithilfe des Profil-Assistenten.](creating-a-profile-by-using-the-profile-wizard.md)
    
  - Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion. Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als der Profil-Assistent zum Konfigurieren der Nachrichtendienste und zum Festlegen von Profileigenschaften. 
    
Platzieren Sie das Setupprogramm in einem festgelegten öffentlichen Verzeichnis. Dies ist wichtig, da die meisten Konfigurationsclients, z. B. die Systemsteuerung, erfordern, dass Benutzer den Namen des Verzeichnisses eingeben. Die Systemsteuerung ruft ein Setupprogramm auf, wenn ein Benutzer auf die Schaltfläche **"Hinzufügen"** klickt, das Dialogfeld **Datenträger** besitzen aufruft und den Pfad zum Programm angibt. Die Systemsteuerung führt das Programm aus und ruft die Einstiegspunktfunktion Ihres Nachrichtendiensts auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_INSTALL festgelegt ist. 
  
> [!CAUTION]
> Da Profile ein expensabler Bestandteil der MAPI-Architektur sind, stellen Sie sicher, dass ihr Installationsprogramm nichts im Standardprofil speichert, das nur schwer neu erstellt werden kann. Es gibt keine Dienstprogramme für die Profilwiederherstellung, für das Verschieben von Profilen von einem Computer auf einen anderen, für die Offlinesicherung oder für die individuelle oder globale Wiederherstellung aus Sicherungskopien. 
  
## <a name="see-also"></a>Siehe auch



[Message Service-Implementierung](message-service-implementation.md)

