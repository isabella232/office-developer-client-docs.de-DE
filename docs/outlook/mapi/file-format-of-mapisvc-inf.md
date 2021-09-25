---
title: Dateiformat von MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.localizationpriority: high
ms.openlocfilehash: b6711b1a77b7741602acf5f96755339682ae0d45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576289"
---
# <a name="file-format-of-mapisvcinf"></a>Dateiformat von MapiSvc.inf

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Datei "MapiSvc.inf" fungiert als zentrale Datenbank für die MAPI-Nachrichtendienst-Konfigurationsinformation. MapiSvc.inf enthält Informationen zu jedem Nachrichtendienst auf der Arbeitsstation, Informationen zu den Dienstanbietern, die zu dem jeweiligen Nachrichtendienst gehören, und Informationen zum MAPI-Subsystem. MapiSvc.inf ist die primäre Informationsquelle für Profile. D. h., wenn ein neues Profil erstellt oder ein vorhandenes geändert wird, werden die relevanten Informationen für jeden Nachrichtendienst oder Dienstanbieter aus MapiSvc.inf kopiert. 
  
MapiSvc.inf wird in verknüpfte hierarchische Abschnitte unterteilt:
  
1. Ein Abschnitt, der Informationen zu allen Profilen enthält. Dieser Abschnitt besteht aus drei Teilen:
    
   - Der **[Services]**-Abschnitt bietet Links zu den jeweiligen nachfolgenden Nachrichtendienst-Abschnitten. 
    
   - Der **[Help File Mappings]**-Abschnitt enthält Informationen zu .HLP-Dateien, die von Nachrichtendiensten bereitgestellt werden. 
    
   - Im **[Default Services]**-Abschnitt sind Nachrichtendienste aufgeführt, die eine Standardinstallation bilden. 
    
2. Ein Abschnitt, der Informationen zu einzelnen Nachrichtendiensten enthält. Die Einträge in diesen Abschnitten enthalten Links zu nachfolgenden Dienstanbieter-Abschnitten.
    
3. Ein Abschnitt, der Informationen zu einzelnen Nachrichtenanbietern eines Nachrichtendienstes enthält.
    
Die folgende Abbildung zeigt den Aufbau einer typischen MapiSvc.inf-Datei. Es gibt drei Nachrichtendienste: AB, MsgService und MS. Der Name auf der rechten Seite des Gleichheitszeichens für jeden Nachrichtendienst ist der Anzeigename des Dienstes. Jeder Nachrichtendienst besitzt einen eigenen Abschnitt an einer anderen Stelle in der Datei, der mit einem oder mehreren Dienstanbieter-Abschnitten verknüpft ist. Es gibt einen Dienstanbieter-Abschnitt für jeden Dienstanbieter, der dem Nachrichtendienst angehört. Die Nachrichtendienste AB und MS sind Einzelanbieterdienste, während drei Dienstanbieter zum MsgService gehören.
  
**Organisation der Datei "MapiSvc.inf"**
  
![Organisation der Datei "MapiSvc.inf"](media/amapi_30.gif "Organisation der Datei &quot;MapiSvc.inf&quot;")
  
MAPI bietet eine strukturierte Version der MapiSvc.inf-Datei, die die Einträge für das MAPI-Teilsystem enthält. Jeder Nachrichtendienstimplementierer fügt Einträge hinzu, die sowohl für den Dienst als auch die Dienstanbieter, die dem Dienst angehören, maßgeblich sind. Einige Einträge sind erforderlich, während andere optional sind. MAPI erfordert z. B., dass Sie den Namen und Pfad jedes Dienstanbieters in Ihrem Nachrichtendienst angeben. Ohne diese Informationen können sie nicht geladen werden.
  
Sie können erforderliche und optionale Informationen im Abschnitt für Ihren Nachrichtendienst und/oder in den Dienstanbieter-Abschnitten hinzufügen. Wo Sie die Informationen zur Beschreibung Ihres Nachrichtendienstes ablegen, hängt von der Anzahl der Dienstanbieter im Dienst ab. Da diese Informationen für jeden Dienstanbieter im Dienst gelten, müssen Sie für alle Anbieter zugänglich sein. Speichern Sie sie im Nachrichtendienst-Abschnitt, der bevorzugten Option oder in allen Dienstanbieter-Abschnitten. Speichern Sie Informationen einmal, um unnötige Replikation zu vermeiden und zu verhindern, dass mehrere Kopien synchronisiert werden müssen.
  
Wenn Ihr Nachrichtendienst ein Einzelanbieterdienst ist, speichern Sie alle Informationen für den Nachrichtendienst im Abschnitt für den Dienstanbieter und nicht im Abschnitt für den Dienst. Der Zugriff auf den Dienstanbieter-Abschnitt erfolgt schneller und direkter als der Zugriff auf den Nachrichtendienst-Abschnitt. 
  
Speichern Sie nur öffentliche Konfigurationsdaten in der MapiSvc.inf-Datei. Informationen, die privat sind oder zusätzlichen Schutz erfordern, wie z. B. Kennwörter oder andere Anmeldeinformationen, sollten in dieser Datei nicht enthalten sein. Speichern Sie entweder gar keine Informationen dieser Art oder bewahren Sie sie im Profil als sichere Eigenschaften auf. Sichere Eigenschaften verfügen über integrierte Schutzfunktionen wie Verschlüsselung.
  
## <a name="reference"></a>Referenz

Weitere Informationen zum Beheben von Fehlern, wenn MAPI eine Anbieter-DLL blockiert, finden Sie unter [So erlauben Sie MAPI, nicht registrierte Anbieter-DLLs zu laden](https://support.microsoft.com/topic/how-to-allow-mapi-to-load-unregistered-provider-dlls-18d9a1cd-d3d7-fa10-473e-5dfd62d38b0d).

