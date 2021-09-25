---
title: Verwenden des Command-Objekts (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63c7b2a572281353e1d498960f9f9ea59b2e6c08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562062"
---
# <a name="using-the-command-object-access"></a>Verwenden des Command-Objekts (Access)


**Gilt für**: Access 2013, Office 2013

Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.

You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset-Gruppen** werden später in diesem und in anderen Kapiteln behandelt. Stellen Sie sich diese derzeit als Tools zum Speichern und Anzeigen von Resultsets vor. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.

Es ist nicht immer erforderlich ein **Command**-Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute**-Methode im **Connection**-Objekt oder die **Open**-Methode im **Recordset**-Objekt verwenden. Allerdings sollten Sie ein **Command**-Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.

> [!NOTE]
> Bestimmte Command-Objekte können ein Resultset als binären Datenstrom oder als einzelnes Record-Objekt zurückgeben, und nicht als Recordset-Objekt, falls dies vom Anbieter unterstützt wird. Außerdem sind manche Command-Objekte nicht für das Zurückgeben von Resultsets vorgesehen (z. B. eine UPDATE-SQL-Abfrage). In diesem Kapitel wird jedoch das typischste Szenario behandelt, nämlich das Ausführen von Command-Objekten, die Ergebnisse in einem Recordset-Objekt zurückgeben. Weitere Informationen zum Zurückgeben von Ergebnissen in Record- oder Stream-Objekten finden Sie in [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).

Dieser Abschnitt enthält die folgenden Themen:

- [Übersicht über das Command-Objekt](command-object-overview.md)
- [Erstellen und Ausführen eines einfachen Befehls](creating-and-executing-a-simple-command.md)
- [Parameter des Command-Objekts](command-object-parameters.md)
- [Aufrufen einer gespeicherten Prozedur mit einem Befehl](calling-a-stored-procedure-with-a-command.md)
- [Benannte Befehle](named-commands.md)
