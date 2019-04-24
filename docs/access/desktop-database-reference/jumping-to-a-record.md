---
title: Springen zu einem Datensatz
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290786"
---
# <a name="jumping-to-a-record"></a>Springen zu einem Datensatz


**Gilt für**: Access 2013, Office 2013

Mit der [Move](move-method-ado.md)-Methode können Sie im **Recordset** -Objekt mithilfe der folgenden Syntax um eine angegebene Anzahl von Datensätzen vorwärts oder rückwärts navigieren:

```vb 
 
oRs.Move NumRecords, Start
```

Die **Move**-Methode wird für alle **Recordset**-Objekte unterstützt.

Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).

Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition vor den ersten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im **Recordset**-Objekt fest (**BOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen rückwärts zu navigieren, obwohl die **BOF**-Eigenschaft bereits **True** ist.

Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition nach dem letzten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset**-Objekt fest (**EOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen vorwärts zu navigieren, obwohl die **EOF**-Eigenschaft bereits **True** ist.

Es wird ein Fehler generiert, wenn Sie die **Move**-Methode in einem leeren **Recordset**-Objekt aufrufen.

Wenn Sie im Argument *Start* ein Lesezeichen übergeben, erfolgt die Navigation relativ zum Datensatz mit diesem Lesezeichen, vorausgesetzt Lesezeichen werden vom **Recordset**-Objekt unterstützt. Ein Lesezeichen erstellen Sie mithilfe der [Bookmark](bookmark-property-ado.md)-Eigenschaft. Ohne Angabe erfolgt die Navigation relativ zum aktuellen Datensatz.

Falls Sie mithilfe der **CacheSize**-Eigenschaft Datensätze vom Anbieter lokal zwischenspeichern, wird durch das Übergeben eines Arguments *NumRecords*, mit dem die aktuelle Datensatzposition außerhalb der aktuellen Gruppe zwischengespeicherter Datensätze verschoben wird, ADO gezwungen, eine neue Datensatzgruppe ausgehend vom Zieldatensatz abzurufen. Die **CacheSize**-Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.

