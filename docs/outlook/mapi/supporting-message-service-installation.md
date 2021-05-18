---
title: Unterstützen der Installation des Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404701"
---
# <a name="supporting-message-service-installation"></a>Unterstützen der Installation des Nachrichtendiensts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Setupprogramm für die Installation des Nachrichtendiensts sollte die folgenden Schritte ausführen:
  
1. Kopieren Sie Nachrichtendienstdateien, z. B. den Nachrichtendienst und die Dienstanbieter-DLLs, von einer CD oder einem Datenträger auf ein lokales Laufwerk auf der Arbeitsstation. Die Dateien, die kopiert werden müssen, hängen vom Nachrichtendienst ab. In der Regel kopieren Sie mindestens eine DLL.
    
2. Fügen Sie der Konfigurationsdatei Mapisvc.inf Einträge hinzu. Weitere Informationen zum Ändern dieser Datei zur Unterstützung der Dienstanbieter in Ihrem Nachrichtendienst finden Sie unter [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
3. Fügen Sie der Systemregistrierung für Nachrichtendienste gegebenenfalls Einträge hinzu. Weitere Informationen dazu, wie die Einträge in der Systemregistrierung angezeigt werden sollen, finden Sie unter [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).
    
4. Erstellen Sie ein Standardprofil, wenn eines noch nicht vorhanden ist, indem Sie eines der folgenden Elemente verwenden:
    
  - Der Profil-Assistent zum Erstellen eines Profils mithilfe der Benutzerinteraktion über eine Reihe von Dialogfelder. Weitere Informationen zur Verwendung des Profil-Assistenten finden Sie unter [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).
    
  - Die Systemsteuerung zum Erstellen eines Profils mithilfe der Benutzerinteraktion. Die Systemsteuerung bietet dem Benutzer mehr Flexibilität als der Profil-Assistent zum Konfigurieren der Nachrichtendienste und Festlegen von Profileigenschaften. 
    
Platzieren Sie das Setupprogramm in einem festgelegten öffentlichen Verzeichnis. Dies ist wichtig, da die meisten Konfigurationsclients, z. B. die Systemsteuerung, den Namen des Verzeichnisses eingeben müssen. Die Systemsteuerung ruft ein Setupprogramm auf,  wenn ein Benutzer  auf die Schaltfläche Hinzufügen klickt, das Dialogfeld Datenträger haben aufruft und den Pfad zum Programm angibt. Die Systemsteuerung führt das Programm aus und ruft die Einstiegspunktfunktion Ihres Nachrichtendiensts auf, der  _ulContext-Parameter_ ist auf MSG_SERVICE_INSTALL. 
  
> [!CAUTION]
> Da Profile ein ernennbarer Bestandteil der MAPI-Architektur sind, müssen Sie sicherstellen, dass in Ihrem Installationsprogramm nichts im Standardprofil gespeichert wird, das nur schwer neu erstellt werden kann. Es gibt keine Dienstprogramme für die Profilwiederherstellung, für das Verschieben von Profilen von einem Computer auf einen anderen, für die off-line-Sicherung oder für die individuelle oder globale Wiederherstellung von Sicherungskopien. 
  
## <a name="see-also"></a>Siehe auch



[Implementierung des Nachrichtendiensts](message-service-implementation.md)

