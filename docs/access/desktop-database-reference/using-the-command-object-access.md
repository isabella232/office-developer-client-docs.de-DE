---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473110"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**Betrifft**: Access 2013 | Office 2013

Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.

Mit dem Command-Objekt können Sie jede Art von Vorgang vom Anbieter anfordern, vorausgesetzt der Anbieter kann die Befehlszeichenfolge ordnungsgemäß interpretieren. Ein gängiger Vorgang für Datenprovider ist das Abfragen einer Datenbank und das Zurückgeben von Datensätzen in einem Recordset-Objekt. Recordset-Objekte werden weiter unten in diesem Kapitel und in anderen Kapiteln behandelt. Stellen Sie sich Recordset-Objekte für den Moment als Tools zum Speichern und Anzeigen von Resultsets vor. Wie bei vielen ADO-Objekten können in Abhängigkeit von der Funktionalität des Anbieters manche Auflistungen, Methoden oder Eigenschaften des Command-Objekts Fehler generieren.

Es ist nicht immer erforderlich ein **Command** -Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute** -Methode im **Connection** -Objekt oder die **Open** -Methode im **Recordset** -Objekt verwenden. Allerdings sollten Sie ein **Command** -Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.


> [!NOTE]
> <P>Bestimmte <STRONG>Command</STRONG>-Objekte können ein Resultset als binären Datenstrom oder als einzelnes <STRONG>Record</STRONG>-Objekt zurückgeben, und nicht als <STRONG>Recordset</STRONG>-Objekt, falls dies vom Anbieter unterstützt wird. Außerdem sind manche <STRONG>Command</STRONG>-Objekte nicht für das Zurückgeben von Resultsets vorgesehen (z. B. eine UPDATE-SQL-Abfrage). In diesem Kapitel wird jedoch das typischste Szenario behandelt, nämlich das Ausführen von <STRONG>Command</STRONG>-Objekten, die Ergebnisse in einem <STRONG>Recordset</STRONG>-Objekt zurückgeben. Weitere Informationen zum Zurückgeben von Ergebnissen in <STRONG>Record</STRONG>- oder <STRONG>Stream</STRONG>-Objekten finden Sie in <A href="chapter-10-records-and-streams.md">Kapitel 10: Datensätze und Datenströme</A>.</P>


