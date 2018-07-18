---
title: Integrieren von MAPI-Formularservercode mit Windows-Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 31f09b1c2f7b23d63e17f59c28b7bcf377b769d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792691"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrieren von MAPI-Formularservercode mit Windows-Code

  
  
**Betrifft**: Outlook 
  
Denken Sie daran, dass Ihr Formular Server eine Win32-Anwendung ist. Es sind einige Aufgaben im Zusammenhang mit Ihrem Formular Server in den Arbeitsspeicher geladen und ordnungsgemäß beendet. Wie alle Windows-Anwendungen ist der Einstiegspunkt für Ihren Server Formular **WinMain** -Funktion. Diese Funktion ist der entsprechenden Stelle die folgenden Aufgaben ausführen: 
  
- Erstellen und Registrieren einer Fensterklasse, damit Ihr Formular Server mit anderen OLE-Komponenten interagieren kann.
    
- Erstellen und Registrieren einer Fensterklasse oder Klassen für Ihr Formular-Objekte von Benutzeroberflächen.
    
- Aufrufen der Funktion ["MAPIInitialize"](mapiinitialize.md) . **"MAPIInitialize"** verarbeitet die erforderliche OLE Initialisierung für Sie ebenfalls. Dies muss einmal pro Instanz des Servers Formular erfolgen. 
    
- Registrieren eine globale Atom mit zeichenfolgendendarstellung des dem Formular Server Klassen-ID (CLSID). Diese Atom sollte für die Lebensdauer des dem Formular Server vorhanden sein.
    
- Aufrufen der OLE-Funktion [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) Ihr Formular Konferenzserver Klasse mit OLE registriert. 
    
- Erstellen ein Hauptfenster Empfang von Nachrichten an. In diesem Fenster muss wahrscheinlich nicht sichtbar sein, da die spezifischen Fenster einzelne Formularobjekten zugeordnet der Benutzer interagiert werden. Klicken Sie im Hauptfenster während der Entwicklung, kann jedoch eine bequeme Möglichkeit für das debugging Ausgabe oder Kontrolle über Ihre Server Formular sein.
    
- Erstellen eine Nachrichtenschleife, die für die Lebensdauer des Servers Formular ausgeführt wird, übersetzen und Verteilung von Windows-Nachrichten zum aktiven Formular-Objekte.
    
Wenn Ihr Formular Server beendet wird, sollten sie die folgenden Aufgaben ausführen:
  
- Rufen Sie die OLE-Funktion [CoRevokeClassObject für die Abmeldung](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) der Nachrichtenklasse OLE-Registrierung widerrufen werden sollen. 
    
- Rufen Sie **MAPIUninitialize** , um den Formular-Server-Verbindung MAPI ordnungsgemäß zu schließen. 
    
- Löschen Sie das globale Atom, das die Zeichenfolgendarstellung der Klassenbezeichner enthält.
    
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

