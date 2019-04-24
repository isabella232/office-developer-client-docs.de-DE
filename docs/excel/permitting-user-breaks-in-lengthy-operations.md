---
title: Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlAbort-Funktion [Excel 2007], Concurrent Tasks [Excel 2007], User Breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310381"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Auch wenn Windows PreEmptive Multitasking verwendet, wobei die Ausführung ihrer Funktionen oder Befehle sehr viel Zeit in Anspruch nehmen kann, empfiehlt es sich, dem Betriebssystem jetzt und wieder Zeit zu geben, um gleichzeitige Aufgaben zu planen. Mit systemeigenen Windows-aufrufen können Sie dies mithilfe der Sleep-Funktion tun. Mithilfe der C-API können Sie dies mithilfe der XlAbort- [Funktion](xlabort.md)tun, die den Prozessor nicht nur für einen Augenblick liefert, sondern auch überprüft, ob der Benutzer die Cancel-Taste gedrückt hat, **ESC**.
  
Die **xlAbort** -Funktion ermöglicht es Ihrem Code daher zu überprüfen, ob der Benutzer den Prozess beenden, die erforderliche Bereinigung ausführen und dann die Steuerung an Excel zurückgeben möchte. Die Funktion ermöglicht auch das Löschen der Unterbrechungsbedingung. Dadurch können Ihre Befehle ein Dialogfeld anzeigen, um zu überprüfen, ob der Benutzer den Befehl beenden möchte. Wenn der Benutzer den Befehl nicht beenden möchte, wird durch Aufrufen der **xlAbort** -Funktion mit dem Argument *false* der Umbruch deaktiviert. (Das Standardargument ist *true* , das einfach die Bedingung überprüft, aber nicht gelöscht wird.) 
  
Sie können die **xlAbort** -Funktion von einer benutzerdefinierten Funktion (UDF) oder von einem XLL-Befehl aus aufrufen. Wenn die **xlAbort** -Funktion in einem UDF **true**zurückgibt und einen Benutzer Bruch erkannt hat, würden Sie in der Regel Short die Funktions Berechnung kürzen und einen Wert zurückgeben, um anzugeben, dass die Berechnung nicht abgeschlossen wurde, vielleichteine Fehlermeldung oder eine NULL. Sie würden die Unterbrechungsbedingung nicht deaktivieren, sodass andere Instanzen von langwierigen Funktionen, die auch diese Bedingung überprüfen, ebenfalls unterbrechen. Excel löscht diese Bedingung implizit, wenn eine Neuberechnung beendet wird.
  
Wenn Sie eine Unterbrechungsbedingung in einem Befehl feststellen, löschen Sie in der Regel die Bedingung, indem Sie die **xlAbort** -Funktion erneut mit dem Argument **false**aufrufen, obwohl Excel diese Bedingung implizit löscht, wenn ein Befehl beendet wird.
  
## <a name="see-also"></a>Siehe auch



[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)

