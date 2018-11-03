---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d55fd58daf13fa0f3995480f35da4ccc0f17ac5c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946685"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="5a6f0-102">Verwenden des Command-Objekts (Access)</span><span class="sxs-lookup"><span data-stu-id="5a6f0-102">Using the Command object (Access)</span></span>


<span data-ttu-id="5a6f0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a6f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a6f0-p101">Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="5a6f0-p102">Mit dem Command-Objekt können Sie jede Art von Vorgang vom Anbieter anfordern, vorausgesetzt der Anbieter kann die Befehlszeichenfolge ordnungsgemäß interpretieren. Ein gängiger Vorgang für Datenprovider ist das Abfragen einer Datenbank und das Zurückgeben von Datensätzen in einem Recordset-Objekt. Recordset-Objekte werden weiter unten in diesem Kapitel und in anderen Kapiteln behandelt. Stellen Sie sich Recordset-Objekte für den Moment als Tools zum Speichern und Anzeigen von Resultsets vor. Wie bei vielen ADO-Objekten können in Abhängigkeit von der Funktionalität des Anbieters manche Auflistungen, Methoden oder Eigenschaften des Command-Objekts Fehler generieren.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="5a6f0-p103">Es ist nicht immer erforderlich ein **Command** -Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute** -Methode im **Connection** -Objekt oder die **Open** -Methode im **Recordset** -Objekt verwenden. Allerdings sollten Sie ein **Command** -Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="5a6f0-114">Bestimmte Befehle können ein Resultset als binären Datenstrom oder als einen einzigen Datensatz und nicht als ein Recordset-Objekt zurück, wenn dies vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="5a6f0-115">Darüber hinaus einige Befehle nicht für die Verwendung von Resultsets überhaupt (beispielsweise eine SQL-Update-Abfrage) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="5a6f0-116">In diesem Kapitel werden das häufigste Szenario jedoch behandelt: Ausführen von Befehlen, die Ergebnisse in einem Recordset-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5a6f0-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="5a6f0-117">Weitere Informationen zum Zurückgeben von Ergebnissen in Datensätze oder Streams finden Sie unter [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="5a6f0-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="5a6f0-118">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5a6f0-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="5a6f0-119">Übersicht über die Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="5a6f0-119">Command Object Overview</span></span>](command-object-overview.md)

- [<span data-ttu-id="5a6f0-120">Erstellen und Ausführen eines einfachen Befehls</span><span class="sxs-lookup"><span data-stu-id="5a6f0-120">Creating and Executing a Simple Command</span></span>](creating-and-executing-a-simple-command.md)

- [<span data-ttu-id="5a6f0-121">Parameter des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="5a6f0-121">Command Object Parameters</span></span>](command-object-parameters.md)

- [<span data-ttu-id="5a6f0-122">Aufrufen einer gespeicherten Prozedur mit einem Befehl</span><span class="sxs-lookup"><span data-stu-id="5a6f0-122">Calling a Stored Procedure with a Command</span></span>](calling-a-stored-procedure-with-a-command.md)

- [<span data-ttu-id="5a6f0-123">Benannte Befehle</span><span class="sxs-lookup"><span data-stu-id="5a6f0-123">Named Commands</span></span>](named-commands.md)
