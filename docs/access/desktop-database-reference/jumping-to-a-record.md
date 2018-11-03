---
title: Springen zu einem Datensatz
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ce27722600ae8a634092612ddf11694faa4ecef
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944473"
---
# <a name="jumping-to-a-record"></a>Springen zu einem Datensatz


**Betrifft**: Access 2013, Office 2013

Mit der [Move](move-method-ado.md)-Methode können Sie im **Recordset** -Objekt mithilfe der folgenden Syntax um eine angegebene Anzahl von Datensätzen vorwärts oder rückwärts navigieren:

```vb 
 
oRs.Move NumRecords, Start
```

Die **Move** -Methode wird für alle **Recordset** -Objekte unterstützt.

Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).

Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition vor den ersten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im **Recordset**-Objekt fest (**BOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen rückwärts zu navigieren, obwohl die **BOF**-Eigenschaft bereits **True** ist.

Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition nach dem letzten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset**-Objekt fest (**EOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen vorwärts zu navigieren, obwohl die **EOF**-Eigenschaft bereits **True** ist.

Beim Aufrufen der **Move** -Methode aus einem leeren **Recordset** -Objekt wird ein Fehler generiert.

Wenn Sie eine Textmarke in das Argument *Start* übergeben, ist die Verschiebung relativ zum Datensatz mit diesem Lesezeichen, vorausgesetzt, dass das **Recordset** -Objekt Lesezeichen unterstützt. Ein Lesezeichen erstellen Sie mithilfe der [Bookmark](bookmark-property-ado.md)-Eigenschaft. Ohne Angabe erfolgt die Navigation relativ zum aktuellen Datensatz.

Bei Verwendung die **CacheSize** -Eigenschaft auf lokal Cache Datensätze aus der Anbieter auf und übergibt ein *NumRecords* -Argument, das die aktuelle Datensatzposition außerhalb der aktuellen Gruppe der zwischengespeicherten Datensätze verschiebt erzwingt, dass ADO Abrufen einer neuen Gruppe von Datensätzen, Starten aus dem Zieldatensatz. Die **CacheSize** -Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.

