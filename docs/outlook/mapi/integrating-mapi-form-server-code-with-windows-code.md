---
title: Integrieren von MAPI-Formular Server Code mit Windows-Code
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
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrieren von MAPI-Formular Server Code mit Windows-Code

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Denken Sie daran, dass es sich beim Formularserver um eine Win32-Anwendung handelt. Daher gibt es einige Aufgaben im Zusammenhang mit dem Laden des Formular Servers in den Arbeitsspeicher und dem sauberen beenden. Wie bei allen Windows-Anwendungen ist der Einstiegspunkt für Ihren Formularserver die **WinMain** -Funktion. Diese Funktion ist geeignet, um die folgenden Aufgaben auszuführen: 
  
- Erstellen und Registrieren einer Fensterklasse, damit der Formularserver mit anderen OLE-Komponenten interagieren kann.
    
- Erstellen und Registrieren einer Fensterklasse oder von Klassen für die Benutzeroberflächen Ihrer Formularobjekte.
    
- Aufrufen der [MAPIInitialize](mapiinitialize.md) -Funktion. **MAPIInitialize** übernimmt außerdem die erforderliche OLE-Initialisierung. Dies muss einmal pro Instanz des Formular Servers erfolgen. 
    
- Registrieren eines globalen Atoms mit einer Zeichenfolgendarstellung der Klassen-ID (CLSID) des Formular Servers. Dieses Atom sollte für die Lebensdauer des Formular Servers vorhanden sein.
    
- Aufrufen der OLE-Funktion [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) , um die Klassen Factory Ihres Formular Servers mit OLE zu registrieren. 
    
- Erstellen eines Hauptfensters zum Empfangen von Nachrichten. Dieses Fenster muss wahrscheinlich nicht sichtbar sein, da der Benutzer mit den bestimmten Fenstern interagiert, die einzelnen Formularobjekten zugeordnet sind. Während der Entwicklung kann das Hauptfenster jedoch eine praktische Möglichkeit zum Debuggen der Ausgabe oder Steuerung des Formular Servers sein.
    
- Erstellen einer Nachrichtenschleife, die für die Lebensdauer des Formular Servers ausgeführt wird und Windows-Nachrichten in Active Form-Objekte übersetzt und sendet.
    
Wenn der Formularserver beendet wird, sollten die folgenden Aufgaben ausgeführt werden:
  
- Rufen Sie die OLE-Funktion [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) auf, um die OLE-Registrierung Ihrer Nachrichtenklasse zu widerrufen. 
    
- Rufen Sie **MAPIUninitialize** auf, um die Verbindung des Formular Servers mit MAPI ordnungsgemäß zu beenden. 
    
- Löschen Sie das globale Atom, das die Zeichenfolgendarstellung des Klassenbezeichners enthält.
    
## <a name="see-also"></a>Siehe auch



[Schreiben von Formular Server Code](writing-form-server-code.md)

