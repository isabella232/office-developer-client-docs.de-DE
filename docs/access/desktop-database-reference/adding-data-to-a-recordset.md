---
title: Hinzufügen von Daten zu einem Recordset
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 45dd7e954a379f732481c7442b205e7fd0bdce6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594489"
---
# <a name="adding-data-to-a-recordset"></a>Hinzufügen von Daten zu einem Recordset

**Gilt für**: Access 2013, Office 2013

Das **Recordset** -Objekt ist wahrscheinlich das am häufigsten verwendete ADO-Objekt. In ADO stellt man sich ein **Recordset** -Objekt am besten als Kombination eines Resultsets aus einer Datenquelle und der zugehörigen Cursorverhalten vor. Auf diese Weise können Sie Daten in ein **Recordset** -Objekt eingeben und dann mit den Methoden und Eigenschaften des **Recordset** -Objekts in den Datenzeilen navigieren, die Werte in den Zeilen anzeigen sowie das Resultset anderweitig bearbeiten.

Dieser Abschnitt befasst sich mit dem Hinzufügen von Daten zum **Recordset** -Objekt. Informationen zum Navigieren in den Daten oder zum Aktualisieren der Daten finden Sie in [Kapitel 4: Bearbeiten von Daten](chapter-4-editing-data.md) und [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md). Sie benötigen nicht immer die erweiterten Funktionen eines **Command** -Objekts, um einem **Recordset** -Objekt das Resultset hinzuzufügen. In vielen Fällen können Sie den Befehl ausführen, indem Sie die **Source** -Eigenschaft im **Recordset** -Objekt festlegen oder aber eine Befehlszeichenfolge an die **Open** -Methode des **Recordset** -Objekts übergeben.

Es gibt verschiedene Möglichkeiten, um Daten aus der Datenquelle einem **Recordset** -Objekt hinzuzufügen. Die verwendete Technik hängt von den Anforderungen Ihrer Anwendung und der angebotenen Funktionalität des Anbieters ab.

