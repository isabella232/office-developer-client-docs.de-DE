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
# <a name="using-the-connection-object-access"></a><span data-ttu-id="a8b42-102">Verwenden des Connection-Objekts (Access)</span><span class="sxs-lookup"><span data-stu-id="a8b42-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="a8b42-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8b42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8b42-p101">Ein **Connection**-Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. In Abhängigkeit von der vom Anbieter unterstützten Funktionalität können bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection**-Objekts nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a8b42-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="a8b42-p102">Vor dem Öffnen eines **Connection**-Objekts müssen Sie bestimmte Informationen zur Datenquelle und zum Verbindungstyp definieren. Der *ConnectionString*-Parameter der **Open**-Methode des **Connection**-Objekts – oder die **ConnectionString**-Eigenschaft im **Connection**-Objekt – enthält gewöhnlich die meisten dieser Informationen. Eine Verbindungszeichenfolge ist eine Abfolge von Buchstaben, mit der eine variable Anzahl von Argumenten definiert wird. Die Argumente – einige sind für ADO erforderlich, andere wiederum anbieterspezifisch – enthalten Informationen, die das **Connection**-Objekt zum Ausführen seiner Aufgaben benötigt. Die Argumente des *ConnectionString*-Parameters werden durch Semikolons (;) getrennt.</span><span class="sxs-lookup"><span data-stu-id="a8b42-p102">Before opening a **Connection** object, you must define certain information about the data source and type of connection. The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information. A connection string is a string of characters that defines a variable number of arguments. The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work. The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="a8b42-p103">In einer Verbindungszeichenfolge können Sie außerdem einen ODBC-Datenquellennamen (Data Source Name, DSN) oder eine universelle Datenverknüpfungsdatei (Universal Data Link, UDL) angeben. Weitere Informationen zu DSNs finden Sie im Abschnitt über Datenquellen in der ODBC-Programmierreferenz. Weitere Informationen zu UDLs finden Sie in der Übersicht zur Datenverknüpfungs-API in der OLE DB-Programmierreferenz.</span><span class="sxs-lookup"><span data-stu-id="a8b42-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*. For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="a8b42-115">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a8b42-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="a8b42-116">Erstellen der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a8b42-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="a8b42-117">Kontrollieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="a8b42-117">Controlling transactions</span></span>](controlling-transactions.md)
