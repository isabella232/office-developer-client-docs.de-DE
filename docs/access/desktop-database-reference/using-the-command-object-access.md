---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1779f2c7e16e2f39a3912f271296c6a7bd0fd550
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861946"
---
# <a name="using-the-command-object-access"></a>Using the Command Object (Access)


**Betrifft**: Access 2013 | Office 2013

Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.

Mit dem Command-Objekt können Sie jede Art von Vorgang vom Anbieter anfordern, vorausgesetzt der Anbieter kann die Befehlszeichenfolge ordnungsgemäß interpretieren. Ein gängiger Vorgang für Datenprovider ist das Abfragen einer Datenbank und das Zurückgeben von Datensätzen in einem Recordset-Objekt. Recordset-Objekte werden weiter unten in diesem Kapitel und in anderen Kapiteln behandelt. Stellen Sie sich Recordset-Objekte für den Moment als Tools zum Speichern und Anzeigen von Resultsets vor. Wie bei vielen ADO-Objekten können in Abhängigkeit von der Funktionalität des Anbieters manche Auflistungen, Methoden oder Eigenschaften des Command-Objekts Fehler generieren.

Es ist nicht immer erforderlich ein **Command** -Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute** -Methode im **Connection** -Objekt oder die **Open** -Methode im **Recordset** -Objekt verwenden. Allerdings sollten Sie ein **Command** -Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.

> [!NOTE]
> Bestimmte Befehle können ein Resultset als binären Datenstrom oder als einen einzigen Datensatz und nicht als ein Recordset-Objekt zurück, wenn dies vom Anbieter unterstützt wird. Darüber hinaus einige Befehle nicht für die Verwendung von Resultsets überhaupt (beispielsweise eine SQL-Update-Abfrage) zurückgegeben. In diesem Kapitel werden das häufigste Szenario jedoch behandelt: Ausführen von Befehlen, die Ergebnisse in einem Recordset-Objekt zurückgeben. Weitere Informationen zum Zurückgeben von Ergebnissen in Datensätze oder Streams finden Sie unter [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).

Dieser Abschnitt enthält die folgenden Themen:

- [Übersicht über die Command-Objekts](command-object-overview.md)

- [Erstellen und Ausführen eines einfachen Befehls](creating-and-executing-a-simple-command.md)

- [Parameter des Command-Objekts](command-object-parameters.md)

- [Aufrufen einer gespeicherten Prozedur mit einem Befehl](calling-a-stored-procedure-with-a-command.md)

- [Benannte Befehle](named-commands.md)
