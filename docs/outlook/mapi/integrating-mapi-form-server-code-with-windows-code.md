---
title: Integrieren von MAPI-Formularservercode in Windows Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332179"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrieren von MAPI-Formularservercode in Windows Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Denken Sie daran, dass ihr Formularserver eine Win32-Anwendung ist. Es gibt also einige Aufgaben im Zusammenhang mit dem Laden des Formularservers in den Arbeitsspeicher und dem sauberen Beenden. Wie alle Windows ist der Einstiegspunkt für Ihren Formularserver die **WinMain-Funktion.** Diese Funktion ist der geeignete Ort, um die folgenden Aufgaben auszuführen: 
  
- Erstellen und Registrieren einer Fensterklasse, damit der Formularserver mit anderen OLE-Komponenten interagieren kann.
    
- Erstellen und Registrieren einer Fensterklasse oder -klassen für die Benutzeroberflächen ihrer Formularobjekte.
    
- Aufrufen der [MAPIInitialize-Funktion.](mapiinitialize.md) **MAPIInitialize** übernimmt auch die erforderliche OLE-Initialisierung für Sie. Dies muss einmal pro Instanz des Formularservers geschehen. 
    
- Registrieren eines globalen Atoms mit einer Zeichenfolgendarstellung der Klassen-ID (CLSID) des Formularservers. Dieses Atom sollte für die Lebensdauer des Formularservers vorhanden sein.
    
- Aufrufen der [OLE-Funktion CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) zum Registrieren der Klassen factory ihres Formularservers bei OLE. 
    
- Erstellen eines Hauptfensters zum Empfangen von Nachrichten. Dieses Fenster muss wahrscheinlich nicht angezeigt werden, da der Benutzer mit den spezifischen Fenstern interagiert, die einzelnen Formularobjekten zugeordnet sind. Während der Entwicklung kann das Hauptfenster jedoch ein bequemer Ort zum Debuggen der Ausgabe oder Steuerung des Formularservers sein.
    
- Erstellen einer Nachrichtenschleife, die für die Lebensdauer des Formularservers ausgeführt wird, Übersetzen und Senden von Windows-Nachrichten an aktive Formularobjekte.
    
Wenn der Formularserver beendet wird, sollten die folgenden Aufgaben ausgeführt werden:
  
- Rufen Sie die OLE-Funktion [CoRevokeClassObject auf,](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) um die OLE-Registrierung Ihrer Nachrichtenklasse zu widerrufen. 
    
- Rufen **Sie MAPIUninitialize auf,** um die Verbindung des Formularservers mit MAPI ordnungsgemäß zu schließen. 
    
- Löschen Sie das globale Atom, das die Zeichenfolgendarstellung des Klassenbezeichners enthält.
    
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

