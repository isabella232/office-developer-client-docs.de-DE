---
title: Befehle, Funktionen und Status in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zustände [Excel 2007],Befehle [Excel 2007],Arbeitsblattfunktionen[Excel 2007],Makrovorlagenfunktionen [Excel 2007],Excel-Zustände
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310969"
---
# <a name="excel-commands-functions-and-states"></a>Excel-Befehle, -Funktionen und -Zustände

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel erkennt zwei sehr verschiedene Arten zusätzlicher Funktionalität: Befehle und Funktionen.
  
## <a name="commands"></a>Befehle

In Excel haben Befehle die folgenden Eigenschaften:
  
- Sie führen Aktionen auf dieselbe Weise durch wie Benutzer.
    
- Sie können alles tun, was ein Benutzer tun kann (innerhalb der Grenzen der verwendeten Benutzeroberfläche), z. B. Excel-Einstellungen ändern, Dokumente öffnen, schließen und bearbeiten, Neuberechnungen initiieren usw.
    
- Sie können so eingerichtet werden, dass sie aufgerufen werden, wenn bestimmte eingeschlossene Ereignisse auftreten.
    
- Sie können Dialogfelder anzeigen und mit dem Benutzer interagieren.
    
- Sie können verknüpft werden, um Objekte zu steuern, sodass sie aufgerufen werden, wenn eine Aktion für das jeweilige Objekt durchgeführt wird, z. B. mit der linken Maustaste klicken.
    
- Sie werden von Excel niemals während einer Neuberechnung aufgerufen.
    
- Sie können während einer Neuberechnung nicht von Funktionen aufgerufen werden.
    
## <a name="functions"></a>Funktionen

Funktionen bewirken in Excel Folgendes:
  
- Sie nehmen in der Regel Argumente an und geben immer ein Ergebnis zurück.
    
- Sie können als Teil einer Excel-Formel in eine oder mehrere Zellen eingegeben werden.
    
- Sie können in definierten Namensdefinitionen verwendet werden.
    
- Sie können in Grenzwert- und Schwellenwertausdrücken für die bedingte Formatierung verwendet werden.
    
- Sie können von Befehlen aufgerufen werden.
    
- Sie können keine Befehle aufrufen.
    
Excel macht einen weiteren Unterschied zwischen benutzerdefinierten Tabellenfunktionen und benutzerdefinierten Funktionen, die auf Makrovorlagen ausgelegt sind. Excel schränkt benutzerdefinierte Makrovorlagenfunktionen nicht auf die reine Verwendung in Makrovorlagen ein: Diese Funktionen können überall dort verwendet werden, wo eine normale Tabellenfunktion verwendet werden kann.
  
### <a name="worksheet-functions"></a>Tabellenfunktionen

Folgendes gilt für Excel-Arbeitsblattfunktionen:
  
- Sie können nicht auf Makrovorlagen-Informationsfunktionen zugreifen.
    
- Sie können nicht die Werte für nicht berechnete Zellen erhalten.
    
- Sie können ab Excel 2007 als threadsicher geschrieben und registriert werden.
    
### <a name="macro-sheet-functions"></a>Makrovorlagenfunktionen

Folgendes gilt für Excel-Makrovorlagenfunktionen:
  
- Sie können auf Makrovorlagen-Informationsfunktionen zugreifen.
    
- Sie können die Werte nicht berechneter Zellen erhalten, einschließlich der Werte der aufrufenden Zellen.
    
- Sie werden ab Excel 2007 nicht als threadsicher eingestuft.
    
Wie Excel eine benutzerdefinierte Funktion behandelt, was die Funktion zulässt und wie die Funktion neu berechnet wird, wird festgelegt, wenn Sie die Funktion registrieren. Wenn eine Funktion als eine Tabellenfunktion registriert ist, jedoch versucht, etwas zu tun, das nur eine Makrovorlagenfunktion durchführen kann, tritt bei dem Vorgang ein Fehler auf. Ab Excel 2007 wird ein Vorgang ebenfalls nicht ausgeführt, wenn eine als threadsicher registrierte Arbeitsblattfunktion versucht, eine Makrovorlagenfunktion aufzurufen.
  
Excel behandelt Microsoft Visual Basic for Applications (VBA) UDFs insofern als makrovorlagenäquivalente Funktionen, als sie auf Arbeitsbereichinformationen und den Wert nicht berechneter Zellen zugreifen können. Zudem gelten sie ab Excel 2007 nicht als threadsicher.
  
## <a name="excel-states"></a>Excel-Zustände

Excel kann sich zu einem bestimmten Zeitpunkt in unterschiedlichen Zuständen befinden, abhängig von den Aktionen des Benutzers, einem externen Prozess, einem abgefangenen Ereignis beim Ausführen eines Makros oder einem zeitlich festgelegten Excel-Housekeepingereignis, z. B. **AutoSpeichern**.
  
Der Benutzer wird auf die folgenden Status treffen:
  
- **Status „Bereit“:** Es werden keine Befehle oder Makros ausgeführt. Es werden keine Dialogfelder angezeigt. Es werden keine Zellen bearbeitet, und der Benutzer ist nicht mitten in einem Vorgang zum Ausschneiden/Kopieren und Einfügen. Kein eingebettetes Objekt besitzt den Fokus. 
    
- **Bearbeitungsmodus:** Der Benutzer hat begonnen, gültige Eingabezeichen in eine nicht gesperrte oder geschützte Zelle einzugeben, oder hat **F2** in einer oder mehreren nicht gesperrten oder geschützten Zellen gedrückt. 
    
- **Auschneiden/Kopieren-und-Einfügen-Modus:** Der Benutzer hat eine Zelle oder einen Zellenbereich ausgeschnitten oder kopiert und noch nicht eingefügt, oder er hat sie über das Dialogfeld „Inhalte einfügen“ eingefügt, das mehrere Einfügevorgänge ermöglicht. 
    
- **Punktmodus:** Der Benutzer bearbeitet eine Formel und wählt Zellen aus, deren Adressen der bearbeiteten Formel hinzugefügt werden. 
    
Der Benutzer kann die Bearbeitungs-, Punkt- und Ausschneiden/Kopieren-Modi löschen, indem der die **ESC**-Taste drückt, wodurch Excel in den Status „Bereit“ zurückkehrt. Auch andere Ereignisse wie die folgenden können diese Status löschen: 
  
- Der Benutzer öffnet ein integriertes Dialogfeld.
    
- Der Benutzer initiiert eine Neuberechnung.
    
- Der Benutzer führt einen Befehl aus.
    
- Excel führt einen **AutoSpeichern**-Vorgang aus. 
    
- Ein Zeitgeberereignis wird eingeschlossen.
    
Das letzte Beispiel ist für Add-In-Entwickler von Bedeutung. Sie sollten die Auswirkungen der normalen Verwendbarkeit von Excel berücksichtigen, bei der häufige Zeitgeberereignistraps festgelegt und ausgeführt werden. Wenn dies ein wichtiger Bestandteil der Funktionalität Ihres Add-Ins ist, sollten Sie Benutzern eine leicht zugängliche Möglichkeit bieten, sie anzuhalten, damit sie bei Bedarf normale Ausschneiden/Kopieren-und-Einfügen-Vorgänge ausführen können.
  
## <a name="see-also"></a>Siehe auch



[Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
[Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)

