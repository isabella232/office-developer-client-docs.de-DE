---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706701"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="65a2c-102">Verwenden des Connection-Objekts (Access)</span><span class="sxs-lookup"><span data-stu-id="65a2c-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="65a2c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65a2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65a2c-p101">Ein **Connection** -Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. In Abhängigkeit von der vom Anbieter unterstützten Funktionalität können bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection** -Objekts nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="65a2c-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="65a2c-107">Vor dem Öffnen eines **Connection** -Objekts müssen Sie bestimmte Informationen zur Datenquelle und zum Verbindungstyp definieren.</span><span class="sxs-lookup"><span data-stu-id="65a2c-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="65a2c-108">Der Parameter *ConnectionString* der **Open** -Methode des **Connection** -Objekts – oder der **ConnectionString** -Eigenschaft auf das **Connection** -Objekt – in der Regel enthält die meisten dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="65a2c-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="65a2c-109">Eine Verbindungszeichenfolge ist eine Abfolge von Buchstaben, mit der eine variable Anzahl von Argumenten definiert wird.</span><span class="sxs-lookup"><span data-stu-id="65a2c-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="65a2c-110">Die Argumente - einige sind für ADO erforderlich, andere wiederum anbieterspezifisch - enthalten Informationen, die das **Connection** -Objekt zum Ausführen seiner Aufgaben benötigt.</span><span class="sxs-lookup"><span data-stu-id="65a2c-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="65a2c-111">Die Argumente, die der *ConnectionString* -Parameter bilden werden mit Semikolons (;) voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="65a2c-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="65a2c-112">Sie können auch eine ODBC-Datenquellennamen (DSN) oder eine Datei Daten Link (UDL) in eine Verbindungszeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="65a2c-112">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string.</span></span> <span data-ttu-id="65a2c-113">Weitere Informationen zu dem DSNs finden Sie unter Datenquellen in Teil 1 von der *ODBC-Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="65a2c-113">For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*.</span></span> <span data-ttu-id="65a2c-114">Weitere Informationen zu UDLs finden Sie unter Data Link API Overview in der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="65a2c-114">For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="65a2c-115">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="65a2c-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="65a2c-116">Erstellen der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65a2c-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="65a2c-117">Steuern von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="65a2c-117">Controlling transactions</span></span>](controlling-transactions.md)
