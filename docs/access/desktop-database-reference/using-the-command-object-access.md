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
# <a name="using-the-command-object-access"></a><span data-ttu-id="0ddd4-102">Using the Command Object (Access)</span><span class="sxs-lookup"><span data-stu-id="0ddd4-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="0ddd4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ddd4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0ddd4-p101">Nachdem Sie eine Verbindung mit einer Datenquelle hergestellt haben, müssen Sie Anforderungen dafür ausführen, um Resultsets zu erhalten. ADO kapselt diese Befehlsfunktionalität im **Command** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ddd4-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="0ddd4-p102">Mit dem Command-Objekt können Sie jede Art von Vorgang vom Anbieter anfordern, vorausgesetzt der Anbieter kann die Befehlszeichenfolge ordnungsgemäß interpretieren. Ein gängiger Vorgang für Datenprovider ist das Abfragen einer Datenbank und das Zurückgeben von Datensätzen in einem Recordset-Objekt. Recordset-Objekte werden weiter unten in diesem Kapitel und in anderen Kapiteln behandelt. Stellen Sie sich Recordset-Objekte für den Moment als Tools zum Speichern und Anzeigen von Resultsets vor. Wie bei vielen ADO-Objekten können in Abhängigkeit von der Funktionalität des Anbieters manche Auflistungen, Methoden oder Eigenschaften des Command-Objekts Fehler generieren.</span><span class="sxs-lookup"><span data-stu-id="0ddd4-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="0ddd4-p103">Es ist nicht immer erforderlich ein **Command** -Objekt zu erstellen, um einen Befehl für eine Datenquelle auszuführen. Sie können die **Execute** -Methode im **Connection** -Objekt oder die **Open** -Methode im **Recordset** -Objekt verwenden. Allerdings sollten Sie ein **Command** -Objekt verwenden, wenn Sie einen Befehl im Code wiederverwenden oder wenn Sie detaillierte Parameterinformationen mit dem Befehl übergeben müssen. Diese Szenarien werden weiter unten in diesem Kapitel ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="0ddd4-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0ddd4-p104">Bestimmte <STRONG>Command</STRONG>-Objekte können ein Resultset als binären Datenstrom oder als einzelnes <STRONG>Record</STRONG>-Objekt zurückgeben, und nicht als <STRONG>Recordset</STRONG>-Objekt, falls dies vom Anbieter unterstützt wird. Außerdem sind manche <STRONG>Command</STRONG>-Objekte nicht für das Zurückgeben von Resultsets vorgesehen (z. B. eine UPDATE-SQL-Abfrage). In diesem Kapitel wird jedoch das typischste Szenario behandelt, nämlich das Ausführen von <STRONG>Command</STRONG>-Objekten, die Ergebnisse in einem <STRONG>Recordset</STRONG>-Objekt zurückgeben. Weitere Informationen zum Zurückgeben von Ergebnissen in <STRONG>Record</STRONG>- oder <STRONG>Stream</STRONG>-Objekten finden Sie in <A href="chapter-10-records-and-streams.md">Kapitel 10: Datensätze und Datenströme</A>.</span><span class="sxs-lookup"><span data-stu-id="0ddd4-p104">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider. Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query). This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object. For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


