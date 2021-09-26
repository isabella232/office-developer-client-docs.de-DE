---
title: Integrieren von MAPI-Formularservercode in Windows Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53213ca6fb5bd22f4d952c317869e707c7034736
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620611"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrieren von MAPI-Formularservercode in Windows Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Denken Sie daran, dass ihr Formularserver eine Win32-Anwendung ist. Daher gibt es einige Aufgaben im Zusammenhang mit dem Laden des Formularservers in den Arbeitsspeicher und dem sauberen Beenden. Wie alle Windows Anwendungen ist der Einstiegspunkt für Ihren Formularserver die **WinMain-Funktion.** Diese Funktion ist der geeignete Ort, um die folgenden Aufgaben auszuführen: 
  
- Erstellen und Registrieren einer Fensterklasse, damit der Formularserver mit anderen OLE-Komponenten interagieren kann.
    
- Erstellen und Registrieren einer Fensterklasse oder -klassen für die Benutzeroberflächen ihrer Formularobjekte.
    
- Aufrufen der [MAPIInitialize-Funktion.](mapiinitialize.md) **MAPIInitialize** verarbeitet auch die erforderliche OLE-Initialisierung für Sie. Dies muss einmal pro Instanz des Formularservers erfolgen. 
    
- Registrieren eines globalen Atoms mit einer Zeichenfolgendarstellung des Klassenbezeichners des Formularservers (CLSID). Dieses Atom sollte für die Lebensdauer des Formularservers vorhanden sein.
    
- Aufrufen der OLE-Funktion ["CoRegisterClassObject",](https://msdn.microsoft.com/library/ms693407.aspx) um die Klassenfactory des Formularservers mit OLE zu registrieren. 
    
- Erstellen eines Hauptfensters zum Empfangen von Nachrichten. Dieses Fenster muss wahrscheinlich nicht sichtbar sein, da der Benutzer mit den spezifischen Fenstern interagiert, die einzelnen Formularobjekten zugeordnet sind. Während der Entwicklung kann das Hauptfenster jedoch ein bequemer Ort zum Debuggen der Ausgabe oder Steuerung des Formularservers sein.
    
- Erstellen einer Nachrichtenschleife, die für die Lebensdauer des Formularservers ausgeführt wird, Übersetzen und Verteilen von Windows-Nachrichten in aktive Formularobjekte.
    
Wenn der Formularserver beendet wird, sollten die folgenden Aufgaben ausgeführt werden:
  
- Rufen Sie die OLE-Funktion [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) auf, um die OLE-Registrierung Ihrer Nachrichtenklasse zu widerrufen. 
    
- Rufen Sie **MAPIUninitialize** auf, um die Verbindung des Formularservers mit mapi ordnungsgemäß zu schließen. 
    
- Löschen Sie das globale Atom, das die Zeichenfolgendarstellung des Klassenbezeichners enthält.
    
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

