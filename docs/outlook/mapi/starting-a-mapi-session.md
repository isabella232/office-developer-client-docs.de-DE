---
title: Starten einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336344"
---
# <a name="starting-a-mapi-session"></a>Starten einer MAPI-Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl beim Starten der Sitzung ein erheblicher Arbeitsaufwand ausgeführt wird, sind die erforderlichen Aufgaben minimal. Ein Teil dieser Arbeit wird in der MAPI-Verarbeitung der [MAPIInitialize-](mapiinitialize.md) und [MAPILogonEx-Aufrufe](mapilogonex.md) erledigt. Beide Funktionen akzeptieren Flags als Eingabeparameter für die Steuerung von Aspekten der Sitzung, z. B. der Benachrichtigungsbehandlung und der Benutzeroberfläche. Es ist wichtig, die Folgen des Festlegens dieser Flags beim Aufrufen von **MAPIInitialize** zu verstehen, um die MAPI-Bibliotheken und **MAPILogonEx** für die Anmeldung am MAPI-Subsystem zu initialisieren. 
  
 **So starten Sie eine MAPI-Sitzung**
  
1. Rufen **Sie MAPIInitialize auf,** um den Standardsatz von MAPI-Bibliotheken zu initialisieren. 
    
2. Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize auf.](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)
    
3. Wenn Sie die MAPI-Hilfsbibliothek verwenden müssen, rufen Sie [ScInitMapiUtil auf.](scinitmapiutil.md)
    
4. Rufen **Sie MAPILogonEx mit** einem gültigen Profil auf, um sich beim MAPI-Subsystem zu anmelden. **MAPILogonEx** überprüft die Konfiguration der einzelnen Dienstanbieter in den Nachrichtendiensten, die im Profil enthalten sind, und fordert den Benutzer auf, bei Bedarf und möglich weitere Informationen zu erhalten. Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten Dienstanbieter für den Dienst bereit. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Initialisieren von MAPI](initializing-mapi.md)
  
> Beschreibt, wie MAPI für eine Sitzung initialisiert wird.
    
[Initialisieren von OLE für MAPI](initializing-ole-for-mapi.md)
  
> Beschreibt die Aufrufe zum Initialisieren von OLE für die Verwendung mit MAPI.
    
[Initialisieren der MAPI-Dienstprogramme](initializing-the-mapi-utilities.md)
  
> Beschreibt das Initialisieren von MAPI-Dienstprogrammen.
    
[Anmelden bei MAPI](logging-on-to-mapi.md)
  
> Beschreibt, wie sich Clientanwendungen beim MAPI-Untersystem anmelden.
    

