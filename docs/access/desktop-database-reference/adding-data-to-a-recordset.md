---
title: Hinzufügen von Daten zu einem Recordset-Objekt
TOCTitle: Adding Data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b013ab0b05242b4928f7a9b9d974ef98ca6103d0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885024"
---
# <a name="adding-data-to-a-recordset"></a>Hinzufügen von Daten zu einem Recordset


**Betrifft**: Access 2013, Office 2013

Das **Recordset** -Objekt ist wahrscheinlich das am häufigsten verwendete ADO-Objekt. In ADO stellt man sich ein **Recordset** -Objekt am besten als Kombination eines Resultsets aus einer Datenquelle und der zugehörigen Cursorverhalten vor. Auf diese Weise können Sie Daten in ein **Recordset** -Objekt eingeben und dann mit den Methoden und Eigenschaften des **Recordset** -Objekts in den Datenzeilen navigieren, die Werte in den Zeilen anzeigen sowie das Resultset anderweitig bearbeiten.

Dieser Abschnitt befasst sich mit dem Hinzufügen von Daten zum **Recordset** -Objekt. Informationen zum Navigieren in den Daten oder zum Aktualisieren der Daten finden Sie in [Kapitel 4: Bearbeiten von Daten](chapter-4-editing-data.md) und [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md). Sie benötigen nicht immer die erweiterten Funktionen eines **Command** -Objekts, um einem **Recordset** -Objekt das Resultset hinzuzufügen. In vielen Fällen können Sie den Befehl ausführen, indem Sie die **Source** -Eigenschaft im **Recordset** -Objekt festlegen oder aber eine Befehlszeichenfolge an die **Open** -Methode des **Recordset** -Objekts übergeben.

Es gibt verschiedene Möglichkeiten, um Daten aus der Datenquelle einem **Recordset** -Objekt hinzuzufügen. Die verwendete Technik hängt von den Anforderungen Ihrer Anwendung und der angebotenen Funktionalität des Anbieters ab.

