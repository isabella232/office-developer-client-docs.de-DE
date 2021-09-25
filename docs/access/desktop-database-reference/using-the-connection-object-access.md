---
title: Verwenden des Connection-Objekts (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a8c7a77903ef318b6ac802c4d1488cc053d4db9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562055"
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
