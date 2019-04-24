---
title: Verwenden des Connection-Objekts (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305922"
---
# <a name="using-the-connection-object-access"></a>Verwenden des Connection-Objekts (Access)


**Gilt für**: Access 2013, Office 2013

Ein **Connection**-Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. In Abhängigkeit von der vom Anbieter unterstützten Funktionalität können bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection**-Objekts nicht verfügbar sein.

Vor dem Öffnen eines **Connection**-Objekts müssen Sie bestimmte Informationen zur Datenquelle und zum Verbindungstyp definieren. Der *ConnectionString*-Parameter der **Open**-Methode des **Connection**-Objekts – oder die **ConnectionString**-Eigenschaft im **Connection**-Objekt – enthält gewöhnlich die meisten dieser Informationen. Eine Verbindungszeichenfolge ist eine Abfolge von Buchstaben, mit der eine variable Anzahl von Argumenten definiert wird. Die Argumente – einige sind für ADO erforderlich, andere wiederum anbieterspezifisch – enthalten Informationen, die das **Connection**-Objekt zum Ausführen seiner Aufgaben benötigt. Die Argumente des *ConnectionString*-Parameters werden durch Semikolons (;) getrennt.

> [!NOTE]
> In einer Verbindungszeichenfolge können Sie außerdem einen ODBC-Datenquellennamen (Data Source Name, DSN) oder eine universelle Datenverknüpfungsdatei (Universal Data Link, UDL) angeben. Weitere Informationen zu DSNs finden Sie im Abschnitt über Datenquellen in der ODBC-Programmierreferenz. Weitere Informationen zu UDLs finden Sie in der Übersicht zur Datenverknüpfungs-API in der OLE DB-Programmierreferenz.

Dieser Abschnitt enthält die folgenden Themen:

- [Erstellen der Verbindungszeichenfolge](creating-the-connection-string.md)
- [Kontrollieren von Transaktionen](controlling-transactions.md)
