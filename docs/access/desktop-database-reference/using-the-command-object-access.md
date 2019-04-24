---
title: Verwenden des Command-Objekts (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312026"
---
# <a name="using-the-command-object-access"></a>Verwenden des Command-Objekts (Access)


**Gilt für**: Access 2013, Office 2013

Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.

You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s wird später in diesem und anderen Kapiteln besprochen; Betrachten Sie Sie im Moment als Tools zum Speichern und Anzeigen von Resultsets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.

Es ist nicht immer erforderlich ein **Command**-Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute**-Methode im **Connection**-Objekt oder die **Open**-Methode im **Recordset**-Objekt verwenden. Allerdings sollten Sie ein **Command**-Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.

> [!NOTE]
> Bestimmte Command-Objekte können ein Resultset als binären Datenstrom oder als einzelnes Record-Objekt zurückgeben, und nicht als Recordset-Objekt, falls dies vom Anbieter unterstützt wird. Außerdem sind manche Command-Objekte nicht für das Zurückgeben von Resultsets vorgesehen (z. B. eine UPDATE-SQL-Abfrage). In diesem Kapitel wird jedoch das typischste Szenario behandelt, nämlich das Ausführen von Command-Objekten, die Ergebnisse in einem Recordset-Objekt zurückgeben. Weitere Informationen zum Zurückgeben von Ergebnissen in Record- oder Stream-Objekten finden Sie in [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).

Dieser Abschnitt enthält die folgenden Themen:

- [Übersicht über das Command-Objekt](command-object-overview.md)
- [Erstellen und Ausführen eines einfachen Befehls](creating-and-executing-a-simple-command.md)
- [Parameter des Command-Objekts](command-object-parameters.md)
- [Aufrufen einer gespeicherten Prozedur mit einem Befehl](calling-a-stored-procedure-with-a-command.md)
- [Benannte Befehle](named-commands.md)
