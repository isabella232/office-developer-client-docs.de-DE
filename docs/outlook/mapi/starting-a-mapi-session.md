---
title: MAPI-Sitzung starten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795623"
---
# <a name="starting-a-mapi-session"></a>MAPI-Sitzung starten

  
  
**Betrifft**: Outlook 
  
Es ist, zwar eine große Menge von Arbeit während der Sitzung starten sind die erforderlichen Aufgaben sehr gering. Viele dieser Aufgaben erfolgt in der MAPI Verarbeitung der Aufrufe der ["MAPIInitialize"](mapiinitialize.md) und [MAPILogonEx](mapilogonex.md) . Beide Funktionen akzeptieren Flags als Eingabeparameter für Aspekte der Sitzung wie Benachrichtigung Behandlung und die Benutzeroberfläche steuern. Es ist wichtig zu verstehen, folgen die Festlegung jedes dieser Flags beim Aufrufen von **"MAPIInitialize"** zum Initialisieren der MAPI-Bibliotheken und **MAPILogonEx** zur Anmeldung bei der MAPI-Subsystems. 
  
 **Zum Starten einer MAPI-Sitzung**
  
1. Rufen Sie **"MAPIInitialize"** , um den Standardsatz von MAPI-Bibliotheken zu initialisieren. 
    
2. Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Wenn Sie die Dienstprogramm MAPI-Bibliothek verwenden müssen, rufen Sie [ScInitMapiUtil](scinitmapiutil.md).
    
4. Rufen Sie mit einem gültigen Profil zur Anmeldung bei der MAPI-Subsystems **MAPILogonEx** . **MAPILogonEx** überprüft die Konfiguration der einzelnen-Dienstanbieter in der Nachrichtendienste im Profil enthalten zusätzliche Informationen der Benutzer aufgefordert wird, bei Bedarf und mögliche. Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten-Dienstanbieter für den Dienst bereit. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[MAPI-Initialisierung](initializing-mapi.md)
  
> Beschreibt, wie MAPI für eine Sitzung nicht initialisiert werden.
    
[Initialisierung von OLE für die MAPI](initializing-ole-for-mapi.md)
  
> Beschreibt die Anrufe tätigen OLE für die Verwendung mit MAPI nicht initialisiert werden.
    
[Initialisieren der MAPI-Dienstprogramme](initializing-the-mapi-utilities.md)
  
> Beschreibt, wie MAPI-Dienstprogramme nicht initialisiert werden.
    
[Anmelden bei MAPI](logging-on-to-mapi.md)
  
> Beschreibt, wie Clientanwendungen mit dem MAPI-Sub System anmelden.
    

