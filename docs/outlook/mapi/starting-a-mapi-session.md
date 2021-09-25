---
title: Starten einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 765bfef3ab30ec4a534f78cc7175394d96d5163c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566381"
---
# <a name="starting-a-mapi-session"></a>Starten einer MAPI-Sitzung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Obwohl während des Sitzungsstarts ein erheblicher Aufwand ausgeführt wird, sind die erforderlichen Aufgaben minimal. Ein Großteil dieser Arbeit erfolgt bei der MAPI-Verarbeitung der [MAPIInitialize-](mapiinitialize.md) und [MAPILogonEx-Aufrufe.](mapilogonex.md) Beide Funktionen akzeptieren Flags als Eingabeparameter zum Steuern von Aspekten der Sitzung, z. B. die Behandlung von Benachrichtigungen und die Benutzeroberfläche. Es ist wichtig zu verstehen, welche Auswirkungen das Festlegen dieser Flags beim Aufrufen von **MAPIInitialize** hat, um die MAPI-Bibliotheken und **MAPILogonEx** für die Anmeldung am MAPI-Subsystem zu initialisieren. 
  
 **So starten Sie eine MAPI-Sitzung**
  
1. Rufen Sie **MAPIInitialize** auf, um den Standardsatz von MAPI-Bibliotheken zu initialisieren. 
    
2. Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)auf.
    
3. Wenn Sie die MAPI-Hilfsprogrammbibliothek verwenden müssen, rufen Sie [ScInitMapiUtil](scinitmapiutil.md)auf.
    
4. Rufen Sie **MAPILogonEx** mit einem gültigen Profil auf, um sich beim MAPI-Subsystem anzumelden. **MAPILogonEx** überprüft die Konfiguration der einzelnen Dienstanbieter in den im Profil enthaltenen Nachrichtendiensten und fordert den Benutzer nach Bedarf und nach Möglichkeit auf, zusätzliche Informationen einzufordern. Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten Dienstanbieter bereit für den Dienst. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Initialisieren von MAPI](initializing-mapi.md)
  
> Beschreibt, wie MAPI für eine Sitzung initialisiert wird.
    
[Initialisieren von OLE für MAPI](initializing-ole-for-mapi.md)
  
> Beschreibt die Aufrufe zum Initialisieren von OLE für die Verwendung mit MAPI.
    
[Initialisieren der MAPI-Dienstprogramme](initializing-the-mapi-utilities.md)
  
> Beschreibt, wie MAPI-Dienstprogramme initialisiert werden.
    
[Anmelden bei MAPI](logging-on-to-mapi.md)
  
> Beschreibt, wie sich Clientanwendungen beim MAPI-Untersystem anmelden.
    

