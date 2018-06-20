---
title: Excel-Befehle,-Funktionen und-Zustände
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zustände [excel 2007], Befehle [Excel 2007], Arbeitsblattfunktionen [Excel 2007], Makroblatt Funktionen [Excel 2007], Excel Staaten
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790425"
---
# <a name="excel-commands-functions-and-states"></a>Excel-Befehle,-Funktionen und-Zustände

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel erkennt zwei sehr unterschiedliche Arten von Funktionalität: Befehle und Funktionen.
  
## <a name="commands"></a>Befehle

In Excel weisen Befehle folgende Merkmale auf:
  
- Sie führen Aktionen auf die gleiche Weise, die Benutzer ausführen.
    
- Sie können alles möglich, ein Benutzer (Betreff auf die Grenzwerte der Schnittstelle verwendet), wie Excel-Einstellungen ändern, öffnen, schließen und Bearbeiten von Dokumenten, initiieren neuberechnungen führen kann und so weiter.
    
- Sie können eingerichtet werden, aufgerufen werden, wenn bestimmte behandelter Ereignisse auftreten.
    
- Sie können Dialogfelder anzeigen und interagieren mit dem Benutzer.
    
- Sie können verknüpft werden, um Objekte zu steuern, sodass sie aufgerufen werden, wenn eine Aktion für dieses Objekt, wie Sie mit der linken Maustaste durchgeführt wird.
    
- Sie werden von Excel nie während einer neuberechnung aufgerufen.
    
- Sie können nicht von Funktionen während einer neuberechnung aufgerufen werden.
    
## <a name="functions"></a>Funktionen

Funktionen in Excel wie folgt vor:
  
- In der Regel Argumente, und geben immer ein Ergebnis zurück.
    
- Sie können in eine oder mehrere Zellen als Teil einer Excel-Formel eingegeben werden.
    
- Sie können in definierter Name Definitionen verwendet werden.
    
- Sie können in bedingten Formatierung Grenzwert und Schwellenwert Ausdrücken verwendet werden.
    
- Sie können mithilfe der Befehle aufgerufen werden.
    
- Sie können Befehle nicht aufrufen.
    
Excel wird einen weiteren Unterschied zwischen benutzerdefinierten Arbeitsblattfunktionen und benutzerdefinierte Funktionen, mit denen Makrovorlagen arbeiten. Excel wird nicht eingeschränkt Makro benutzerdefinierte Funktionen nur für auf Makroblättern verwendet wird: Diese Funktionen können überall dort verwendet werden eine normalen Tabellenfunktion verwendet werden kann.
  
### <a name="worksheet-functions"></a>Arbeitsblattfunktionen

Das folgende gilt für Excel-Arbeitsblattfunktionen:
  
- Sie können nicht Makro Blatt Informationsfunktionen zugreifen.
    
- Sie können nicht der Werte von Zellen gekennzeichnete erhalten.
    
- Diese werden geschrieben und als threadsicheren ab Excel 2007 registriert.
    
### <a name="macro-sheet-functions"></a>Makrovorlage Funktionen

Das folgende gilt der Excel-Makrovorlage Funktionen:
  
- Sie können Funktionen Makro Informationen zugreifen.
    
- Sie können die Werte der gekennzeichnete Zellen, einschließlich der Werte der aufrufenden Zellen zu erhalten.
    
- Sie sind nicht Thread sicherer ab Excel 2007 betrachtet.
    
Wie Excel eine benutzerdefinierte Funktion (UDF) behandelt, was die Funktion genehmigt und wie diese neu berechnet die Funktion sind alle bestimmt wird, wenn Sie die Funktion registrieren. Wenn eine Funktion als einer Tabellenfunktion registriert ist er versucht, etwas, das nur eine Makrovorlage Funktion möglich ist, schlägt der Vorgang fehl. Ab Excel 2007, wenn eine Tabellenfunktion als threadsicheren registriert versucht, eine Makro Blatt-Funktion aufgerufen, fällt erneut, der Vorgang aus.
  
Excel behandelt Microsoft Visual Basic für Applikationen (VBA) UDFs wie Makro Blatt Entsprechung-Funktionen, um die Arbeitsbereichsinformationen und der Wert der gekennzeichnete Zellen zugreifen können, und sie gelten nicht als wie thread sicherer ab Excel 2007.
  
## <a name="excel-states"></a>Excel-Status

Excel kann zu einem bestimmten Zeitpunkt gemäß den Aktionen des Benutzers, einen externen Prozess, ein abgefangener Ereignis Ausführen eines Makros oder einer Excel Wartungsaufgaben terminierte wie **Automatisches Speichern**in einer Reihe von Staaten sein.
  
Die Zustände, die das Benutzererlebnis lauten wie folgt:
  
- **Status bereit:** Keine Befehle oder Makros werden ausgeführt. Es werden keine Dialogfelder angezeigt wird. Keine Zellen bearbeitet werden, und der Benutzer ist nicht in der Mitte eines Vorgangs Ausschneiden/Kopieren und einfügen. Kein eingebettetes Objekt besitzt den Fokus. 
    
- **Bearbeitungsmodus:** Der Benutzer gestartet wurde, in eine Zelle ungeschützt sind oder keine gültige Eingabezeichen eingeben oder auf eine oder mehrere ungeschützt sind oder keine Zellen **F2** gedrückt. 
    
- **Modus Ausschneiden/Kopieren und einfügen:** Der Benutzer ausgeschnitten oder kopiert eine Zelle oder eines Zellbereichs hat und sie nicht noch eingefügt wurde, oder sie über das Dialogfeld Inhalte einfügen, wodurch mehrere Einfügevorgänge eingefügt. 
    
- **Punktmodus:** Der Benutzer wird eine Formel zu bearbeiten, und ist Markieren von Zellen, die die Formel bearbeitet, deren Adressen hinzugefügt werden. 
    
Der Benutzer kann die bearbeiten, Point und Ausschneiden/Kopieren Modi deaktivieren, durch Drücken von **ESC** -Taste, die in den Zustand bereit Excel zurückgibt. Andere Ereignisse können die Zustände, wie die folgenden deaktivieren: 
  
- Der Benutzer öffnet ein integriertes Dialogfeld.
    
- Der Benutzer versucht, eine neuberechnung.
    
- Der Benutzer führt einen Befehl.
    
- Excel führt eine **Automatische Speicherung** ausgeführt. 
    
- Es wird ein Timer-Ereignis aufgefangen.
    
Das letzte Beispiel ist von Bedeutung für Add-In-Entwickler. Sie sollten die Auswirkung der normalen Anwendungsfunktionen für Excel, in dem häufig verwendete Timer-Ereignis Trapping ausgeführt wird, sind wird festlegen und ausgeführt. Wenn dies einen wichtigen Bestandteil von Add-in Funktionalität ist, sollten Sie Benutzer mit Weise leicht zugänglich anhalten, sodass sie können Ausschneiden/Kopieren und Einfügen normalerweise bei Bedarf bereitstellen.
  
## <a name="see-also"></a>Siehe auch



[Excel-Programmierkonzepte](excel-programming-concepts.md)
  
[Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge](permitting-user-breaks-in-lengthy-operations.md)

