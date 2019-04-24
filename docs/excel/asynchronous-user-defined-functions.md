---
title: Asynchrone benutzerdefinierte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7fdf3bd09914981865c911fd65a78d044ad582f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304172"
---
# <a name="asynchronous-user-defined-functions"></a>Asynchrone benutzerdefinierte Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 kann benutzerdefinierte Funktionen asynchron aufrufen. Das asynchrone Aufrufen von Funktionen kann die Leistung verbessern, da mehrere Berechnungen gleichzeitig ausgeführt werden können. Wenn Sie benutzerdefinierte Funktionen in einem Computecluster ausführen, können dank asynchroner Funktionsaufrufe mehrere Computer für die Durchführung von Berechnungen verwendet werden.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Verwendungsmöglichkeiten für asynchrone benutzerdefinierte Funktionen

Einige benutzerdefinierte Funktionen müssen auf externe Ressourcen warten. Während des Wartens wird der Thread für Excel-Berechnungen blockiert. In Excel 2013 können benutzerdefinierte Funktionen asynchron ausgeführt werden. Dadurch wird der Berechnungs Thread für die Ausführung anderer Berechnungen freigegeben, während die benutzerdefinierte Funktion wartet.
  
In Excel 2007 können Programmierer mehrere benutzerdefinierte Funktionen gleichzeitig ausführen, indem Sie die Anzahl der Threads erhöhen, die bei Neuberechnungen mit mehreren Threads verwendet werden. Diese Methode weist hauptsächlich Nachteile auf, da die Anzahl der Threads eine Einstellung ist, die auf eine Anwendung begrenzt ist und nicht auf Ebene einer einzelnen Funktion oder eines Add-ins gesteuert werden kann.
  
Programmierer sollten asynchrone benutzerdefinierte Funktionsaufrufe verwenden, wenn die Funktion auf externe Ressourcen warten muss. Eine Funktion, die eine SOAP-Anforderung über das Internet sendet, muss beispielsweise warten, bis das Netzwerk die Anforderung übermittelt, den Remoteserver, um die Anforderung abzuschließen, und das Netzwerk, um das Ergebnis zurückzugeben. In diesem Fall gibt es keine nennenswerten Rechenvorgänge, und Excel kann mit anderen Berechnungen fortfahren.
  
Programmierer können auch asynchrone benutzerdefinierte Funktionen verwenden, wenn eine Funktion Anforderungen an einen Compute-Cluster sendet. In diesem Fall muss nicht nur auf die Netzwerkwartezeit gewartet werden, sondern der Cluster kann separate Aufrufe auf separaten Servern ausführen. Wenn Sie nicht darauf warten, dass jeder Anruf beendet wird, können die Aufrufe überlagert werden, um die Leistung zu verbessern. In einigen Fällen ist diese Verbesserung erheblich.
  
> [!NOTE]
> Benutzerdefinierte Funktionen können nicht sowohl als asynchroner als auch als Cluster sicher registriert werden. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Schreiben einer asynchronen benutzerdefinierten Funktion

Asynchrone benutzerdefinierte Funktionen müssen ein Handle verfolgen und dieses Handle verwenden, wenn Sie Excel informieren, dass der Funktionsaufruf abgeschlossen ist. Eine asynchrone benutzerdefinierte Funktion ist in zwei Teile aufgeteilt. Das erste Element ist der standardmäßige UDF-Einstiegspunkt, der einen zweiten, separaten asynchronen Vorgang startet. Rückrufe in Excel sollten während des UDF-Einstiegspunkts vorgenommen werden. Der erste Startteil der Funktion gibt dann die Steuerung des Berechnungs Threads an Excel zurück, wodurch die Berechnung fortgesetzt wird. Wenn der zweite asynchrone Vorgang abgeschlossen ist, muss er zurück in Excel aufrufen und Excel mit seinem Ergebnis bereitstellen. 
  
> [!NOTE]
> Alle an das UDF übergebenen Argumente, die von dem asynchronen Teil der Funktion benötigt werden, müssen tief kopiert werden, da Excel diese Argumente freilässt, wenn der UDF-Einstiegspunkt zurückgegeben wird. 
  
Excel bietet eine Reihe von Ereignissen, die ein XLL-Add-in verwenden kann, um den Lebenszyklus von asynchronen UDF-aufrufen zu verwalten. Diese Ereignisse zeigen an, dass Excel mit Berechnungen abgeschlossen ist oder dass die Berechnung abgebrochen wurde.
  
### <a name="declaring-an-asynchronous-function"></a>Deklarieren einer asynchronen Funktion

Sie müssen asynchrone benutzerdefinierte Funktionen als asynchron deklarieren, wenn Sie registriert sind. Dies wird durch Hinzufügen eines Parameters, der auf eine XLOPER12-Struktur verweist, die durch "X" in der Registrierungstyp Zeichenfolge dargestellt wird, an beliebiger Stelle in der Liste der UDF-Parameter ausgeführt. Excel verwendet diesen Parameter, um das asynchrone Anruf Handle zu übergeben. Das XLL-Add-in muss den asynchronen Anruf Handle und das Ergebnis der Funktion an Excel zurückgeben, wenn das Ergebnis bereit ist. Darüber hinaus sollte der Rückgabetyp des UDF **void**sein, gekennzeichnet durch ">" als erstes Zeichen in der Zeichenfolge. Der Rückgabetyp ist ungültig, da der synchrone Teil des UDF keinen Wert an Excel zurückgibt. Stattdessen gibt das XLL-Add-in einen Wert asynchron über einen Rückruf zurück. 
  
Sie können asynchrone Funktionen als threadsicher deklarieren und dann wird der synchrone Teil des UDF in einer Neuberechnung mit mehreren Threads verwendet. 
  
Das folgende Codebeispiel zeigt eine asynchrone benutzerdefinierte Funktion, die mit "\>QX" als Registrierungszeichenfolge registriert ist:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Zurückgeben von Werten

Wenn das Ergebnis des asynchronen Aufrufs bereit ist, gibt das XLL-Add-in das Ergebnis an Excel zurück, indem ein Rückruf vom Typ [xlAsyncReturn](xlasyncreturn.md)ausgeführt wird.
  
**xlAsyncReturn** ist der einzige Rückruf, den Sie bei der Neuberechnung für nicht-Berechnungs-Threads verwenden können. Daher sollte der asynchrone Teil einer asynchronen UDF keine anderen Rückrufe ausführen. 
  
### <a name="handling-events"></a>Behandeln von Ereignissen

Ab Excel 2010 können XLLs Ereignisse empfangen, die zum Verwalten des asynchronen Funktions Lebenszyklus entwickelt wurden. Weitere Informationen finden Sie unter [Behandeln von Ereignissen](handling-events.md).
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von XLLs für Excel](developing-excel-xlls.md)

