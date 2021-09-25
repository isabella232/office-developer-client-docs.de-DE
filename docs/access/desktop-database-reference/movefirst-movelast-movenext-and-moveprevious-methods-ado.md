---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3e4c0ba5e5475ccf957eb63056fb38940864caa4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593957"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a>MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (ADO)


**Gilt für**: Access 2013, Office 2013

Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt. Mithilfe dieser Funktionen wird dieser Datensatz zum aktuellen Datensatz.

## <a name="syntax"></a>Syntax

*Recordset*. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **MoveFirst**-Methode, um die aktuelle Position des Datensatzes an die Position des ersten Datensatzes im **Recordset**-Objekt zu verschieben.

Verwenden Sie die **MoveLast** -Methode, um die aktuelle Position des Datensatzes an die Position des letzten Datensatzes im **Recordset** -Objekt zu verschieben. Das **Recordset** -Objekt muss Textmarken oder die rückwärtsgerichtete Verschiebung des Cursors unterstützen. Andernfalls wird beim Aufrufen der Methode ein Fehler generiert.

A call to either **MoveFirst** or **MoveLast** when the **Recordset** is empty (both **BOF** and **EOF** are True) generates an error.

Verwenden Sie die **MoveNext**-Methode, um die aktuelle Position des Datensatzes um einen Datensatz nach vorn zu verschieben (zum Ende des **Recordset**-Objekts). Wenn es sich beim letzten Datensatz um den aktuellen Datensatz handelt und die **MoveNext**-Methode aufgerufen wird, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset**-Objekt fest ([EOF](bof-eof-properties-ado.md) hat den Wert **True**). Beim Versuch, den Datensatz nach vorn zu verschieben, wenn die **EOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert.

Wenn **Recordset** -Objekt gefiltert oder sortiert wird und die Daten des aktuellen Datensatzes geändert wurden, ändert sich die Position möglicherweise ebenso. In solchen Fällen wird die **MoveNext** -Methode ordnungsgemäß ausgeführt, aber Sie sollten wissen, dass die Position von der neuen Position (und nicht von der vorherigen Position) aus um einen Datensatz nach vorn verschoben wird. Wenn Sie beispielsweise die Daten im aktuellen Datensatz so ändern, dass der Datensatz an das Ende des sortierten Recordsets verschoben **wird,** bedeutet dies, dass durch aufrufen von **MoveNext** in ADO der aktuelle Datensatz auf die Position nach dem letzten Datensatz im **Recordset** festgelegt wird (**EOF**  =  **True**).

Verwenden Sie die **MovePrevious**-Methode, um die aktuelle Position des Datensatzes um einen Datensatz nach hinten zu verschieben (zum Anfang des **Recordset**-Objekts). Das **Recordset**-Objekt muss Textmarken oder die rückwärtsgerichtete Verschiebung des Cursors unterstützen. Andernfalls wird beim Aufrufen der Methode ein Fehler generiert. Wenn es sich beim ersten Datensatz um den aktuellen Datensatz handelt und die **MovePrevious**-Methode aufgerufen wird, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im **Recordset**-Objekt fest ([BOF](bof-eof-properties-ado.md) weist den Wert **True** auf). Beim Versuch, den Datensatz nach hinten zu verschieben, wenn die **BOF**-Eigenschaft bereits auf **True** festgelegt ist, wird ein Fehler generiert. Unterstützt das **Recordset**-Objekt weder Textmarken noch eine rückwärtsgerichtete Verschiebung des Cursors, generiert die **MovePrevious**-Methode einen Fehler.

Ist das **Recordset**-Objekt vorwärtsgerichtet, und Sie möchten, dass der vorwärtsgerichtete und der rückwärtsgerichtete Bildlauf unterstützt wird, können Sie die [CacheSize](cachesize-property-ado.md)-Eigenschaft verwenden, um einen Datensatzcache zu erstellen, der eine rückwärtsgerichtete Verschiebung des Cursors mithilfe der [Move](move-method-ado.md)-Methode unterstützt. Da zwischengespeicherte Datensätze in den Speicher geladen werden, sollten Sie nur so viele Datensätze wie erforderlich zwischenspeichern. Sie können die **MoveFirst**-Methode in einem vorwärtsgerichteten **Recordset**-Objekt aufrufen, wodurch der Anbieter den Befehl, mit dem das **Recordset**-Objekt generiert wird, möglicherweise erneut ausführt.

