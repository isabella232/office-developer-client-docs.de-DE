---
title: Asynchrone benutzerdefinierte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5b64dfd4308da4efb5e94010fe1dc9d758a1199c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790378"
---
# <a name="asynchronous-user-defined-functions"></a>Asynchrone benutzerdefinierte Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 können benutzerdefinierte Funktionen asynchron aufrufen. Asynchron aufrufen von Funktionen kann Leistung verbessern, indem mehrere Berechnungen zur selben Zeit ausführen zulassen. Beim Ausführen von benutzerdefinierten Funktionen in einem Computecluster ermöglicht das Aufrufen von Funktionen asynchron mehrere Computer verwendet werden, um die Berechnungen abgeschlossen.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Verwendung von asynchronen benutzerdefinierten Funktionen

Externe Ressourcen müssen einige benutzerdefinierte Funktionen warten. Während sie warten, wird der Excel-Berechnung-Thread blockiert. Benutzerdefinierte Funktionen können in Excel 2013 asynchron ausgeführt. Dadurch werden den Berechnung Thread zum anderen Berechnungen ausführen, während die benutzerdefinierte Funktion wartet.
  
In Excel 2007 konnte Programmierer mehrere benutzerdefinierte Funktionen zur selben Zeit ausführen, indem Sie sich eine Erhöhung der Anzahl von Threads in mehreren Threads neuberechnungen verwendet. Diese Methode hat Nachteile in erster Linie, da die Anzahl der Threads eine Einstellung zu einer Anwendung ausgelegt ist und kann nicht auf der Ebene der eine einzige Funktion oder ein Add-in gesteuert werden.
  
Programmierer sollten asynchrone benutzerdefinierte Funktion Anrufe verwenden, wenn die Funktion für externe Ressourcen warten muss. Beispielsweise muss eine Funktion, die eine SOAP-Anforderung über das Internet sendet für das Netzwerk übermittelt die Anforderung, den Remoteserver für die Durchführung die Anforderung und des Netzwerks und das Ergebnis zurückgegeben warten. In diesem Fall ist keine signifikanten Netzwerke auftritt und Excel kann mit anderen Berechnungen fortfahren.
  
Programmierer können auch asynchrone benutzerdefinierte Funktionen verwenden, wenn eine Funktion Anfragen an einem Computecluster sendet. In diesem Fall ist nicht nur die Netzwerklatenz bedürfen, aber der Cluster kann separate Anrufe auf separaten Servern ausführen. Durch nicht für jeden Anruf beendet wartet, können die Anrufe überlappt werden zur Verbesserung der Leistung. In einigen Fällen ist diese Verbesserung von Bedeutung.
  
> [!NOTE]
> Benutzerdefinierte Funktionen konnte nicht registriert werden, als die asynchrone und sichere cluster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Schreiben einer asynchronen benutzerdefinierten Funktion

Asynchrone benutzerdefinierte Funktionen müssen verfolgen an ein Handle und verwenden dieses Handle Excel darüber informiert, dass der Funktionsaufruf abgeschlossen ist. Eine asynchrone benutzerdefinierte Funktion ist in zwei Bereiche unterteilt. Der erste Teil ist der standard UDF-Einstiegspunkt, der eine zweite, separate asynchrone Operation gestartet wird. Rückrufe in Excel soll während der UDF-Einstiegspunkt erfolgen. Der erste Start Teil der Funktion gibt Steuerung seiner Berechnung Thread zu Excel zurück, der Berechnung weiterhin. Wenn der zweite asynchrone Vorgang abgeschlossen ist, muss es Rückruf in Excel und Excel durch das Ergebnis bereitzustellen. 
  
> [!NOTE]
> Alle Argumente an die UDF übergeben, die vom asynchronen Teil erforderlich sind die Funktion Tiefe muss kopiert, da Excel folgende Argumente freigegeben, wenn der UDF-Einstiegspunkt zurückgegeben. 
  
Excel bietet eine Reihe von Ereignissen, die ein XLL-add-in verwenden können, um den Lebenszyklus von asynchrone UDF-Aufrufe zu verwalten. Diese Ereignisse bedeuten, dass Excel Berechnungen abgeschlossen ist oder die Berechnung abgebrochen wurde.
  
### <a name="declaring-an-asynchronous-function"></a>Deklarieren eine asynchrone-Funktion

Sie müssen die asynchrone benutzerdefinierte Funktionen als asynchron deklarieren, wenn sie registriert sind. Dies erfolgt, indem Sie einen Parameter, der zeigt auf eine Struktur XLOPER12, dargestellt durch "X" in der Registrierung Typ String an einer beliebigen Stelle in der Liste der UDF-Parameter hinzufügen. Excel verwendet diesen Parameter, um den asynchronen Aufruf Handle übergeben. Des XLL-add-Ins muss übergeben Sie das Handle asynchronen Aufruf und das Ergebnis der Funktion zu Excel Wenn das Ergebnis bereit ist. Darüber hinaus der Rückgabetyp der UDF-Datei sollte nicht **void**, genehmigtes ">" als das erste Zeichen in der Zeichenfolge. Der Rückgabetyp ist nichtig, da der synchrone Teil der UDF nicht nach Excel einen Wert zurückgibt. In diesem Fall gibt des XLL-add-Ins einen Wert asynchron über einen Rückruf. 
  
Sie können asynchrone Funktionen deklarieren, als threadsicheren und dann der synchrone Teil der UDF-Datei in eine Multithread-neuberechnung verwendet wird. 
  
Das folgende Codebeispiel zeigt eine asynchrone benutzerdefinierte Funktion registriert mithilfe von "\>QX" als die Registrierung Typ String:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Rückgabe von Werten

Wenn das Ergebnis des asynchronen Aufrufs bereit ist, gibt das XLL-add-in das Ergebnis an Excel Datenquellenanbieters führen Sie einen Rückruf von Typ [XlAsyncReturn](xlasyncreturn.md).
  
**XlAsyncReturn** ist der einzige Rückruf, die, den Sie während einer neuberechnung auf nicht-Berechnungsthreads verwenden können. Daher sollte der asynchrone Teil einer asynchronen UDF keine anderen Rückrufe durchführen. 
  
### <a name="handling-events"></a>Behandeln von Ereignissen

Ab Excel 2010 können XLLs Ereignisse im Lebenszyklus des asynchronen Funktion verwalten soll empfangen. Weitere Informationen finden Sie unter [Behandeln von Ereignissen](handling-events.md).
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Excel-XLLs](developing-excel-xlls.md)

