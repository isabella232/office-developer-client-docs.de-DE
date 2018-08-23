---
title: Staren einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e95423a1aa9a04247a70592a797d2395cafecc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595370"
---
# <a name="starting-a-mapi-session"></a>Staren einer MAPI-Sitzung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Es ist, zwar eine große Menge von Arbeit während der Sitzung starten sind die erforderlichen Aufgaben sehr gering. Viele dieser Aufgaben erfolgt in der MAPI Verarbeitung der Aufrufe der ["MAPIInitialize"](mapiinitialize.md) und [MAPILogonEx](mapilogonex.md) . Beide Funktionen akzeptieren Flags als Eingabeparameter für Aspekte der Sitzung wie Benachrichtigung Behandlung und die Benutzeroberfläche steuern. Es ist wichtig zu verstehen, folgen die Festlegung jedes dieser Flags beim Aufrufen von **"MAPIInitialize"** zum Initialisieren der MAPI-Bibliotheken und **MAPILogonEx** zur Anmeldung bei der MAPI-Subsystems. 
  
 **Zum Starten einer MAPI-Sitzung**
  
1. Rufen Sie **"MAPIInitialize"** , um den Standardsatz von MAPI-Bibliotheken zu initialisieren. 
    
2. Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Wenn Sie die Dienstprogramm MAPI-Bibliothek verwenden müssen, rufen Sie [ScInitMapiUtil](scinitmapiutil.md).
    
4. Rufen Sie mit einem gültigen Profil zur Anmeldung bei der MAPI-Subsystems **MAPILogonEx** . **MAPILogonEx** überprüft die Konfiguration der einzelnen-Dienstanbieter in der Nachrichtendienste im Profil enthalten zusätzliche Informationen der Benutzer aufgefordert wird, bei Bedarf und mögliche. Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten-Dienstanbieter für den Dienst bereit. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Initialisieren von MAPI](initializing-mapi.md)
  
> Beschreibt, wie MAPI für eine Sitzung nicht initialisiert werden.
    
[Initialisieren von OLE für MAPI](initializing-ole-for-mapi.md)
  
> Beschreibt die Anrufe tätigen OLE für die Verwendung mit MAPI nicht initialisiert werden.
    
[Initialisieren der MAPI-Dienstprogramme](initializing-the-mapi-utilities.md)
  
> Beschreibt, wie MAPI-Dienstprogramme nicht initialisiert werden.
    
[Anmelden bei MAPI](logging-on-to-mapi.md)
  
> Beschreibt, wie Clientanwendungen mit dem MAPI-Sub System anmelden.
    

