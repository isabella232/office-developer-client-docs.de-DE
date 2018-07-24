---
title: Excel-Befehle, -Funktionen und -Zustände
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zustände [Excel 2007],Befehle [Excel 2007],Arbeitsblattfunktionen[Excel 2007],Makrovorlagenfunktionen [Excel 2007],Excel-Zustände
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790425"
---
# <a name="excel-commands-functions-and-states"></a>Excel-Befehle, -Funktionen und -Zustände

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel erkennt zwei sehr verschiedene Typen von Zusatzfunktionen: Befehle und Funktionen.
  
## <a name="commands"></a>Befehle

In Excel besitzen Befehle die folgenden Merkmale:
  
- Sie führen Aktionen auf die gleiche Weise aus wie Benutzer.
    
- Sie können dieselben Aktionen ausführen wie ein Benutzer (mit den Einschränkungen der verwendeten Benutzeroberfläche), z. B. Excel-Einstellungen ändern, Dokumente öffnen, schließen und bearbeiten, Neuberechnungen auslösen usw.
    
- Sie können so eingerichtet werden, dass sie bei Auftreten bestimmter abgefangener Ereignisse aufgerufen werden.
    
- Sie können Dialogfelder anzeigen und mit dem Benutzer interagieren.
    
- Sie können mit Steuerelementobjekten verknüpft werden, sodass sie bei einer bestimmten Aktion für das Objekt, z. B. einem Linksklick mit der Maus, aufgerufen werden.
    
- Sie werden von Excel nie während einer Neuberechnung aufgerufen.
    
- Sie können von Funktionen nicht während einer Neuberechnung aufgerufen werden.
    
## <a name="functions"></a>Funktionen

Für Funktionen in Excel gilt Folgendes:
  
- Sie akzeptieren in der Regel Argumente und geben immer ein Ergebnis zurück.
    
- Sie können als Teil einer Excel-Formel in eine oder mehrere Zellen eingegeben werden.
    
- Sie können in Definitionen definierter Namen verwendet werden.
    
- Sie können im Grenzwert für bedingte Formatierung und Schwellenwertausdrücken verwendet werden.
    
- Sie können von Befehlen aufgerufen werden.
    
- Sie können keine Befehle aufrufen.
    
Excel macht einen weiteren Unterschied zwischen benutzerdefinierten Arbeitsblattfunktionen und benutzerdefinierten Funktionen, die für die Verwendung in Makrovorlagen entworfen werden. In Excel sind benutzerdefinierte Makrovorlagenfunktionen nicht auf die Verwendung in Makrovorlagen beschränkt: Diese Funktionen können überall dort verwendet werden, wo eine normale Arbeitsblattfunktion verwendet werden kann.
  
### <a name="worksheet-functions"></a>Arbeitsblattfunktionen

Für Excel-Arbeitsblattfunktionen gilt Folgendes:
  
- Sie können nicht auf Makrovorlagen-Informationsfunktionen zugreifen.
    
- Sie können nicht die Werte nicht berechneter Zellen abrufen.
    
- Sie können ab Excel 2007 als threadsicher geschrieben und registriert werden.
    
### <a name="macro-sheet-functions"></a>Makrovorlagenfunktionen

Für Excel-Makrovorlagenfunktionen gilt Folgendes:
  
- Sie können auf Makrovorlagen-Informationsfunktionen zugreifen.
    
- Sie können die Werte nicht berechneter Zellen einschließlich der Werte der aufrufenden Zellen abrufen.
    
- Sie werden ab Excel 2007 nicht als threadsicher eingestuft.
    
Wie Excel eine benutzerdefinierte Funktion (UDF) behandelt, welche Aktionen die Funktion ausführen darf und wie die Funktion neu berechnet wird, wird bestimmt, wenn Sie die Funktion registrieren. Wenn eine Funktion als Arbeitsblattfunktion registriert ist, aber eine Aktion auszuführen versucht, die nur eine Makrovorlagenfunktion ausführen kann, schlägt der Vorgang fehl. Ab Excel 2007 wird ein Vorgang ebenfalls nicht ausgeführt, wenn eine als threadsicher registrierte Arbeitsblattfunktion versucht, eine Makrovorlagenfunktion aufzurufen.
  
Excel behandelt Microsoft Visual Basic for Applications (VBA) UDFs insofern als makrovorlagenäquivalente Funktionen, als sie auf Arbeitsbereichinformationen und den Wert nicht berechneter Zellen zugreifen können. Zudem gelten sie ab Excel 2007 nicht als threadsicher.
  
## <a name="excel-states"></a>Excel-Zustände

Excel kann sich zu einem bestimmten Zeitpunkt in unterschiedlichen Zuständen befinden, abhängig von den Aktionen des Benutzers, einem externen Prozess, einem abgefangenen Ereignis beim Ausführen eines Makros oder einem zeitlich festgelegten Excel-Housekeepingereignis, z. B. **AutoSpeichern**.
  
Folgende Status können beim Benutzer auftreten:
  
- **Status „Bereit“:** Es werden keine Befehle oder Makros ausgeführt. Keine Dialogfelder werden angezeigt. Es werden keine Zellen bearbeitet, und der Benutzer befindet sich nicht mitten in einem Ausschneiden/Kopieren-und-Einfügen-Vorgang. Kein eingebettetes Objekt besitzt den Fokus. 
    
- **Bearbeitungsmodus:** Der Benutzer hat mit der Eingabe gültiger Zeichen in eine nicht gesperrte und nicht geschützte Zelle begonnen oder hat **F2** für eine oder mehrere nicht geschützte und nicht gesperrte Zellen gedrückt. 
    
- **Ausschneiden/Kopieren-und-Einfügen-Modus:** Der Benutzer hat eine Zelle oder einen Zellbereich ausgeschnitten oder kopiert und sie noch nicht eingefügt, oder er hat sie über das Dialogfeld „Inhalte einfügen“ eingefügt, das mehrere Einfügevorgänge ermöglicht. 
    
- **Punktmodus:** Der Benutzer bearbeitet eine Formel und wählt Zellen aus, deren Adressen der bearbeiteten Formel hinzugefügt werden. 
    
Der Benutzer kann den Bearbeitungs-, Punkt- und Ausschneiden/Kopieren-Modus durch Drücken der **ESC**-Taste deaktivieren, wodurch Excel in den Zustand „Bereit“ zurückversetzt wird. Durch folgende Ereignisse können diese Zustände ebenfalls aufgehoben werden: 
  
- Der Benutzer öffnet ein integriertes Dialogfeld.
    
- Der Benutzer initiiert eine Neuberechnung.
    
- Der Benutzer führt einen Befehl aus.
    
- Excel führt einen **AutoSpeichern**-Vorgang aus. 
    
- Es wird ein Timer-Ereignis abgefangen.
    
Das letzte Beispiel ist besonders wichtig für Add-In-Entwickler. Sie sollten die Auswirkungen der normalen Nutzung von Excel berücksichtigen, bei der häufige Timer-Ereignistraps festgelegt und ausgeführt werden. Wenn dies ein wichtiger Bestandteil der Funktionalität Ihres Add-Ins ist, sollten Sie Benutzern eine leicht zugängliche Möglichkeit bieten, sie anzuhalten, damit sie bei Bedarf normale Ausschneiden/Kopieren-und-Einfügen-Vorgänge ausführen können.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)

