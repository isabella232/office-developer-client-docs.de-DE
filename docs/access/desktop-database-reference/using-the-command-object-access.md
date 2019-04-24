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
# <a name="using-the-command-object-access"></a><span data-ttu-id="e04d6-102">Verwenden des Command-Objekts (Access)</span><span class="sxs-lookup"><span data-stu-id="e04d6-102">Using the Command object (Access)</span></span>


<span data-ttu-id="e04d6-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e04d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e04d6-p101">Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e04d6-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="e04d6-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span><span class="sxs-lookup"><span data-stu-id="e04d6-106">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly.</span></span> <span data-ttu-id="e04d6-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="e04d6-107">A common operation for data providers is to query a database and return records in a **Recordset** object.</span></span> <span data-ttu-id="e04d6-108">**Recordset**s wird später in diesem und anderen Kapiteln besprochen; Betrachten Sie Sie im Moment als Tools zum Speichern und Anzeigen von Resultsets.</span><span class="sxs-lookup"><span data-stu-id="e04d6-108">**Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets.</span></span> <span data-ttu-id="e04d6-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span><span class="sxs-lookup"><span data-stu-id="e04d6-109">As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="e04d6-p103">Es ist nicht immer erforderlich ein **Command**-Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute**-Methode im **Connection**-Objekt oder die **Open**-Methode im **Recordset**-Objekt verwenden. Allerdings sollten Sie ein **Command**-Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="e04d6-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="e04d6-114">Bestimmte Command-Objekte können ein Resultset als binären Datenstrom oder als einzelnes Record-Objekt zurückgeben, und nicht als Recordset-Objekt, falls dies vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e04d6-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="e04d6-115">Außerdem sind manche Command-Objekte nicht für das Zurückgeben von Resultsets vorgesehen (z. B. eine UPDATE-SQL-Abfrage).</span><span class="sxs-lookup"><span data-stu-id="e04d6-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="e04d6-116">In diesem Kapitel wird jedoch das typischste Szenario behandelt, nämlich das Ausführen von Command-Objekten, die Ergebnisse in einem Recordset-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e04d6-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="e04d6-117">Weitere Informationen zum Zurückgeben von Ergebnissen in Record- oder Stream-Objekten finden Sie in [Kapitel 10: Datensätze und Datenströme](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e04d6-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="e04d6-118">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e04d6-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="e04d6-119">Übersicht über das Command-Objekt</span><span class="sxs-lookup"><span data-stu-id="e04d6-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="e04d6-120">Erstellen und Ausführen eines einfachen Befehls</span><span class="sxs-lookup"><span data-stu-id="e04d6-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="e04d6-121">Parameter des Command-Objekts</span><span class="sxs-lookup"><span data-stu-id="e04d6-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="e04d6-122">Aufrufen einer gespeicherten Prozedur mit einem Befehl</span><span class="sxs-lookup"><span data-stu-id="e04d6-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="e04d6-123">Benannte Befehle</span><span class="sxs-lookup"><span data-stu-id="e04d6-123">Named commands</span></span>](named-commands.md)
