---
title: Genehmigungsverfahren Benutzer Zeilenumbrüche in langen Vorgänge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Bereichsgröße-Funktion [excel 2007], gleichzeitige Aufgaben [Excel 2007], Benutzer Breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790558"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>Genehmigungsverfahren Benutzer Zeilenumbrüche in langen Vorgänge

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Obwohl Windows unterbrechen Multitasking verwendet wird, in dem können Ihre Funktionen oder Befehle eine auszuführende Zeit, ist es empfehlenswert, einige Zeit für das Betriebssystem und wieder, die es planen gleichzeitige Aufgaben unterstützen ergeben. Systemeigenen Windows-Anrufe verwenden, können Sie hierzu mithilfe der Funktion dem Standbymodus. Der C-API verwenden, können Sie tun sie mithilfe der [Bereichsgröße-Funktion](xlabort.md), die nicht nur den Prozessor für eine Sofortnachrichtensitzung ergibt, sondern auch überprüft, ob der Benutzer die Cancel-Taste **ESC-Taste**gedrückt wurde.
  
Die Funktion **Bereichsgröße** kann daher Code, um zu überprüfen, ob der Benutzer möchte, beenden Sie den Prozess, führen Sie die erforderliche Bereinigung, und klicken Sie dann die Steuerung an Excel zurückzugeben. Die Funktion können auch die Unterbrechung zu deaktivieren. Auf diese Weise können die Befehle zum Anzeigen eines Dialogfelds, um zu überprüfen, ob der Benutzer den Befehl beenden möchte. Wenn der Benutzer nicht den Befehl beenden möchten, löscht die **Bereichsgröße** -Funktion mit dem Argument *FALSE* Aufrufen den Umbruch. (Das Argument der Standardwert ist *TRUE* , die einfach überprüft die Bedingung jedoch nicht gelöscht.) 
  
Sie können die Funktion **Bereichsgröße** aus einer benutzerdefinierten Funktion (UDF) oder aus einem XLL-Befehl aufrufen. In einer UDF beenden die **Bereichsgröße** Funktion **TRUE**, dass eine Unterbrechung Benutzer erkannt können Sie in der Regel die Funktion Berechnung abgeschnitten und einige Wert, um anzugeben, dass die Berechnung nicht wurde abgeschlossen, möglicherweise ein Fehler oder 0 (null) zurück. Sie möchten nicht, die Unterbrechung, damit andere Instanzen des langen Funktionen, die diese Bedingung ferner Seitenumbruch auch deaktivieren. Excel löscht implizit diese Bedingung, wenn eine neuberechnung endet.
  
Wenn Sie eine Unterbrechung in einem Befehl nicht erkennen, löschen Sie Sie in der Regel die Bedingung durch Aufrufen der **Bereichsgröße** Funktion erneut mit dem Argument **FALSE**, obwohl Excel diese Bedingung implizit gelöscht, wenn ein Befehl abgeschlossen wird.
  
## <a name="see-also"></a>Siehe auch



[C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Entwickeln von Excel-XLLs](developing-excel-xlls.md)
  
[Zugriff auf Excel-Instanz und im Hauptfenster von Handles](how-to-access-excel-instance-and-main-window-handles.md)

