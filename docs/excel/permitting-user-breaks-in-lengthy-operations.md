---
title: Zulassen von Benutzerunterbrechungen bei längeren Vorgängen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdaa4fa7212dddf330b1b6159f9eceefc88b2090
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611301"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Zulassen von Benutzerunterbrechungen bei längeren Vorgängen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Auch wenn Windows preemptives Multitasking verwendet, bei dem die Ausführung Ihrer Funktionen oder Befehle sehr viel Zeit in Anspruch nehmen kann, empfiehlt es sich, dem Betriebssystem immer wieder Zeit zu bieten, um gleichzeitige Aufgaben zu planen. Mit systemeigenen Windows Aufrufen können Sie dies mithilfe der Ruhezustandsfunktion tun. Mithilfe der C-API können Sie dies mithilfe der [xlAbort-Funktion](xlabort.md)tun, die nicht nur den Prozessor für einen Moment liefert, sondern auch überprüft, ob der Benutzer die Abbruchtaste , **ESC,** gedrückt hat.
  
Mit der **XlAbort-Funktion** kann Ihr Code daher überprüfen, ob der Benutzer den Prozess beenden, die erforderliche Bereinigung durchführen und dann die Steuerung an Excel zurückgeben möchte. Mit der Funktion können Sie auch die Unterbrechungsbedingung löschen. Dadurch können Ihre Befehle ein Dialogfeld anzeigen, um zu überprüfen, ob der Benutzer den Befehl beenden möchte. Wenn der Benutzer den Befehl nicht beenden möchte, wird durch Aufrufen der **xlAbort-Funktion** mit dem Argument  *FALSE*  der Umbruch gelöscht. (Das Standardargument ist  *TRUE*  , das einfach die Bedingung überprüft, aber nicht löscht.) 
  
Sie können die **xlAbort-Funktion** über eine benutzerdefinierte Funktion (UDF) oder über einen XLL-Befehl aufrufen. Wenn die **XlAbort-Funktion** in einer UDF **TRUE** zurückgibt und eine Benutzerunterbrechung erkannt hat, würden Sie in der Regel die Berechnung der Funktion kürzen und einen Wert zurückgeben, um anzugeben, dass die Berechnung nicht abgeschlossen wurde, z. B. ein Fehler oder null. Sie würden die Unterbrechungsbedingung nicht löschen, sodass auch andere Instanzen von langen Funktionen, die diese Bedingung ebenfalls überprüfen, beschädigt werden. Excel löscht diese Bedingung implizit, wenn eine Neuberechnung endet.
  
Wenn Sie eine Unterbrechungsbedingung in einem Befehl erkennen, löschen Sie die Bedingung in der Regel, indem Sie die **XlAbort-Funktion** erneut mit dem Argument **FALSE** aufrufen, obwohl Excel diese Bedingung implizit löscht, wenn ein Befehl beendet wird.
  
## <a name="see-also"></a>Siehe auch



[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)
  
[Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)

