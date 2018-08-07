---
title: Entwickeln von XLLs für Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Add-Ins – [excel 2007],Entwickeln von XLLs – [Excel 2007],XLLs – [Excel 2007], Entwickeln
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790403"
---
# <a name="developing-excel-xlls"></a>Entwickeln von XLLs für Excel

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Hauptgrund für das Schreiben von Microsoft Excel XLLs und verwenden der C-API ist die Erstellung von Hochleistungs-Tabellenfunktionen. Die Anwendungsszenarien leistungsstarker Funktionen – und ab Excel 2007 die Möglichkeit, Multithread-Schnittstellen auf leistungsstarke Serverressourcen zu schreiben – machen sie zu einem wichtigen Bestandteil der Excel-Erweiterbarkeit. Die Leistung von XLLs wurde in Excel 2007 durch das Hinzufügen neuer Datentypen und die Unterstützung von Multithreading weiter verbessert.
  
Die C-API verfügt nicht über die leistungsstarken Features zur schnellen Entwicklung von Microsoft Visual Basic for Applications (VBA) über COM oder Microsoft .NET Framework. Die Speicherverwaltung ist lediglich rudimentär, weswegen mehr Verantwortung beim Entwickler liegt. Viele Excel-Features, die über COM durch VBA und .NET Framework verfügbar sind, sind in der C-API nicht verfügbar.


- [Konzepte der Excel-Programmierung](excel-programming-concepts.md)
  
- [Arbeiten mit DLLs](working-with-dlls.md)
  
- [Zugreifen auf XLL-Code in Excel](accessing-xll-code-in-excel.md)
  
- [Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Aufrufen von Excel von der DLL oder XLL aus](calling-into-excel-from-the-dll-or-xll.md)
  
- [Erstellen von XLLs](creating-xlls.md)
  
- [Auswerten von Namen und anderen Arbeitsblatt-Formelausdrücken](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Multithreading und Speicherverwaltung](multithreading-and-memory-management.md)
  
- [Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)
  
- [Clustersichere Funktionen](cluster-safe-functions.md)
  
- [Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)
  
- [Anzeigen von Dialogfeldern aus einer DLL oder XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Abwärtskompatibilität](backward-compatibility.md)
  

