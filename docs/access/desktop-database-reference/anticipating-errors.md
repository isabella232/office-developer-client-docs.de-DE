---
title: Vorhersehen von Fehlern
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4bd130ca05527c7761ca587781c1fd4f939ebe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297172"
---
# <a name="anticipating-errors"></a>Vorhersehen von Fehlern


**Gilt für**: Access 2013, Office 2013

Die Fehlervermeidung ist mindestens so wichtig wie die Fehlerbehandlung. Dieser letzte Abschnitt enthält eine kurze Aufstellung der Vorsichtsmaßnahmen für Ihre Anwendung, um die Wahrscheinlichkeit von Fehlern zu reduzieren.

Überprüfen Sie den Status von Objekten, indem Sie den Wert der **State** -Eigenschaft überprüfen, bevor Sie einen Vorgang mithilfe dieser Objekte ausführen. Wenn die Anwendung z. B. ein globales **Connection** -Objekt verwendet, überprüfen Sie dessen **State** -Eigenschaft, um festzustellen, ob es bereits geöffnet ist, bevor Sie die **Open** -Methode aufrufen.

- Jedes Programm, das Daten von einem Benutzer annimmt, muss Code zum Überprüfen dieser Daten enthalten, bevor sie an den Datenspeicher gesendet werden. Sie können sich nicht darauf verlassen, dass Sie vom Datenspeicher, vom Anbieter, von ADO oder sogar von der Programmiersprache über Probleme informiert werden. Sie müssen jedes von den Benutzern eingegebene Byte überprüfen und sicherstellen, dass die Daten den richtigen Typ für das Feld aufweisen und dass erforderliche Felder nicht leer sind.

Überprüfen Sie die Daten, bevor Sie versuchen, Daten in den Datenspeicher zu schreiben. Dazu verwenden Sie am einfachsten das Ereignis **WillMove** oder **WillUpdateRecordset**. Ausführlichere Informationen zum Behandeln von ADO-Ereignissen finden Sie in [Kapitel 7: Behandeln von ADO-Ereignissen](chapter-7-handling-ado-events.md).

Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.

Fehler treten ebenfalls auf, wenn Sie z. B. versuchen, **Seek** oder **Find** für ein leeres **Recordset**-Objekt auszuführen.

