---
title: Asynchrone benutzerdefinierte Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab505a5f929ecc258d39abea6ff9553998bb6b01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614626"
---
# <a name="asynchronous-user-defined-functions"></a>Asynchrone benutzerdefinierte Funktionen

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 können benutzerdefinierte Funktionen asynchron aufrufen. Das asynchrone Aufrufen von Funktionen kann die Leistung verbessern, indem mehrere Berechnungen gleichzeitig ausgeführt werden können. Wenn Sie benutzerdefinierte Funktionen in einem Computecluster ausführen, können dank asynchroner Funktionsaufrufe mehrere Computer für die Durchführung von Berechnungen verwendet werden.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Verwendung von asynchronen benutzerdefinierten Funktionen

Einige benutzerdefinierte Funktionen müssen auf externe Ressourcen warten. Während sie warten, wird der Excel Berechnungsthread blockiert. In Excel 2013 können benutzerdefinierte Funktionen asynchron ausgeführt werden. Dadurch wird der Berechnungsthread freigegeben, um andere Berechnungen auszuführen, während die benutzerdefinierte Funktion wartet.
  
In Excel 2007 konnten Programmierer mehrere benutzerdefinierte Funktionen gleichzeitig ausführen, indem sie die Anzahl der Threads erhöhen, die in Mehrfachthread-Neuberechnungen verwendet werden. Diese Methode hat in erster Linie Nachteile, da die Anzahl der Threads eine Einstellung ist, die auf eine Anwendung beschränkt ist und nicht auf der Ebene einer einzelnen Funktion oder eines Add-Ins gesteuert werden kann.
  
Programmierer sollten asynchrone benutzerdefinierte Funktionsaufrufe verwenden, wenn die Funktion auf externe Ressourcen warten muss. Beispielsweise muss eine Funktion, die eine SOAP-Anforderung über das Internet sendet, warten, bis das Netzwerk die Anforderung übermittelt, der Remoteserver, um die Anforderung abzuschließen, und das Netzwerk, um das Ergebnis zurückzugeben. In diesem Fall tritt keine erhebliche Berechnung auf, und Excel können mit anderen Berechnungen fortfahren.
  
Programmierer können auch asynchrone benutzerdefinierte Funktionen verwenden, wenn eine Funktion Anforderungen an einen Computecluster sendet. In diesem Fall muss nicht nur auf die Netzwerklatenz gewartet werden, sondern der Cluster kann separate Aufrufe auf separaten Servern ausführen. Da nicht gewartet wird, bis jeder Anruf abgeschlossen ist, können die Aufrufe überlappen, um die Leistung zu verbessern. In einigen Fällen ist diese Verbesserung erheblich.
  
> [!NOTE]
> Benutzerdefinierte Funktionen können nicht sowohl als asynchron als auch als clustersicher registriert werden. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Schreiben einer asynchronen benutzerdefinierten Funktion

Asynchrone benutzerdefinierte Funktionen müssen ein Handle nachverfolgen und dieses Handle verwenden, wenn Excel informiert wird, dass der Funktionsaufruf abgeschlossen ist. Eine asynchrone benutzerdefinierte Funktion wird in zwei Teile aufgeteilt. Der erste Teil ist der Standard-UDF-Einstiegspunkt, der einen zweiten, separaten asynchronen Vorgang startet. Rückrufe in Excel sollten während des UDF-Einstiegspunkts erfolgen. Der erste Startteil der Funktion gibt dann die Steuerung des Berechnungsthreads an Excel zurück, wodurch die Berechnung fortgesetzt wird. Wenn der zweite asynchrone Vorgang abgeschlossen ist, muss er in Excel zurückrufen und Excel mit seinem Ergebnis bereitstellen. 
  
> [!NOTE]
> An die UDF übergebene Argumente, die vom asynchronen Teil der Funktion benötigt werden, müssen tief kopiert werden, da Excel diese Argumente freigibt, wenn der UDF-Einstiegspunkt zurückgegeben wird. 
  
Excel bietet eine Reihe von Ereignissen, die ein XLL-Add-In verwenden kann, um den Lebenszyklus asynchroner UDF-Aufrufe zu verwalten. Diese Ereignisse deuten darauf hin, dass Excel mit Berechnungen abgeschlossen wurde oder dass die Berechnung abgebrochen wurde.
  
### <a name="declaring-an-asynchronous-function"></a>Deklarieren einer asynchronen Funktion

Sie müssen asynchrone benutzerdefinierte Funktionen als asynchron deklarieren, wenn sie registriert werden. Dazu wird ein Parameter hinzugefügt, der auf eine XLOPER12-Struktur zeigt, dargestellt durch "X" in der Registrierungstypzeichenfolge, an einer beliebigen Stelle in der Liste der UDF-Parameter. Excel verwendet diesen Parameter, um das asynchrone Aufrufhandle zu übergeben. Das XLL-Add-In muss das asynchrone Aufrufhandle und das Ergebnis der Funktion an Excel übergeben, wenn das Ergebnis bereit ist. Darüber hinaus sollte der Rückgabetyp der UDF **"void"** sein, der durch ">" als erstes Zeichen in der Typzeichenfolge festgelegt wird. Der Rückgabetyp ist ungültig, da der synchrone Teil der UDF keinen Wert an Excel zurückgibt. Stattdessen gibt das XLL-Add-In einen Wert asynchron über einen Rückruf zurück. 
  
Sie können asynchrone Funktionen als threadsicher deklarieren, und dann wird der synchrone Teil der UDF in einer Multithread-Neuberechnung verwendet. 
  
Das folgende Codebeispiel zeigt eine asynchrone benutzerdefinierte Funktion, die mit \> "QX" als Registrierungstypzeichenfolge registriert wurde:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Zurückgeben von Werten

Wenn das Ergebnis des asynchronen Aufrufs bereit ist, gibt das XLL-Add-In das Ergebnis an Excel zurück, indem ein Rückruf vom Typ [xlAsyncReturn](xlasyncreturn.md)ausgeführt wird.
  
**xlAsyncReturn** ist der einzige Rückruf, den Sie während der Neuberechnung für Nicht-Berechnungsthreads verwenden können. Daher sollte der asynchrone Teil einer asynchronen UDF keine anderen Rückrufe ausführen. 
  
### <a name="handling-events"></a>Handhabung von Ereignissen

Ab Excel 2010 können XLLs Ereignisse empfangen, die zum Verwalten des Lebenszyklus asynchroner Funktionen entworfen wurden. Weitere Informationen finden Sie unter [Behandeln von Ereignissen.](handling-events.md)
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln von XLLs für Excel](developing-excel-xlls.md)

