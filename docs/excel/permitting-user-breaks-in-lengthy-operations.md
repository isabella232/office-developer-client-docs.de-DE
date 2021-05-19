---
title: Zulässige Benutzerumbrüche in langwierigen Vorgängen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort-Funktion [excel 2007],gleichzeitige Aufgaben [Excel 2007],Benutzerumbrüche [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414690"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Zulässige Benutzerumbrüche in langwierigen Vorgängen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Auch wenn Windows präemptives Multitasking verwendet, bei dem die Ausführung Ihrer Funktionen oder Befehle sehr lange dauern kann, sollten Sie dem Betriebssystem immer wieder Zeit geben, um gleichzeitige Aufgaben zu planen. Mithilfe von systemeigenen Windows können Sie dies mithilfe der Sleep-Funktion tun. Mithilfe der C-API können Sie dies mithilfe der [xlAbort-Funktion](xlabort.md)tun, die nicht nur den Prozessor für einen Moment ergibt, sondern auch überprüft, ob der Benutzer die Abbruchtaste ESC gedrückt **hat.**
  
Mit **der xlAbort-Funktion** kann Ihr Code daher überprüfen, ob der Benutzer den Prozess beenden, die erforderlichen Bereinigungen tun und dann die Steuerung an Excel. Mit der Funktion können Sie auch die Unterbrechungsbedingung löschen. Auf diese Weise können Die Befehle ein Dialogfeld anzeigen, um zu überprüfen, ob der Benutzer den Befehl beenden möchte. Wenn der Benutzer den Befehl nicht beenden möchte, wird die Unterbrechung durch Aufrufen der **xlAbort-Funktion** mit dem Argument  *FALSE*  beendet. (Das Standardargument ist  *TRUE*  , das die Bedingung einfach überprüft, aber nicht deaktiviert.) 
  
Sie können die **xlAbort-Funktion** über eine benutzerdefinierte Funktion (USERF) oder über einen XLL-Befehl aufrufen. Wenn die **xlAbort-Funktion** in einem UDF **TRUE** zurückgibt, nachdem Sie eine Benutzerumbruch erkannt haben, würden Sie in der Regel die Funktionsberechnung kürzen und einen Wert zurückgeben, der angibt, dass die Berechnung nicht abgeschlossen wurde, z. B. einen Fehler oder null. Sie würden die Unterbrechungsbedingung nicht löschen, sodass auch andere Instanzen langwieriger Funktionen, die diese Bedingung überprüfen, nicht mehr funktionierten. Excel diese Bedingung implizit ab, wenn eine Neuberechnung endet.
  
Wenn Sie eine Unterbrechungsbedingung in einem Befehl erkennen, löschen Sie die Bedingung in der Regel, indem Sie die **xlAbort-Funktion** erneut mit dem Argument **FALSE** aufrufen, obwohl Excel diese Bedingung implizit beendet, wenn ein Befehl endet.
  
## <a name="see-also"></a>Siehe auch



[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)

