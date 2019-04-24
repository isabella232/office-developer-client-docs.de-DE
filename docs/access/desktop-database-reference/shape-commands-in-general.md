---
title: Shape-Befehle im Allgemeinen
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 399836158084f07b30b06a9fb099da74527d0cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308652"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="5205d-102">Shape-Befehle im Allgemeinen</span><span class="sxs-lookup"><span data-stu-id="5205d-102">Shape commands in general</span></span>

<span data-ttu-id="5205d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5205d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5205d-104">Durch Datenstrukturierung werden die Spalten eines geformten **Recordset** -Objekts, die Beziehungen zwischen den durch die Spalten dargestellten Entitäten und die Methode, mit der das **Recordset** -Objekt mit Daten aufgefüllt wird, definiert.</span><span class="sxs-lookup"><span data-stu-id="5205d-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="5205d-105">Ein geformtes **Recordset**-Objekt kann aus den folgenden Spaltentypen bestehen.</span><span class="sxs-lookup"><span data-stu-id="5205d-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5205d-106">Spaltentyp</span><span class="sxs-lookup"><span data-stu-id="5205d-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="5205d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5205d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5205d-108">data</span><span class="sxs-lookup"><span data-stu-id="5205d-108">data</span></span></p></td>
<td><p><span data-ttu-id="5205d-109">Felder eines <strong>Recordset</strong>-Objekts, die von einem Abfragebefehl an einen Datenprovider, eine Tabelle oder ein vorher geformtes <strong>Recordset</strong>-Objekt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5205d-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5205d-110">Kapitel</span><span class="sxs-lookup"><span data-stu-id="5205d-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="5205d-p101">Ein Verweis auf ein anderes <strong>Recordset</strong>-Objekt, das als <em>Kapitel</em> bezeichnet wird. Kapitelspalten ermöglichen des Definieren einer <em>Übergeordnet-Untergeordnet</em>-Beziehung, in der das <em>übergeordnete</em> Element das <strong>Recordset</strong>-Objekt ist, das die Kapitelspalte enthält, und das <em>untergeordnete</em> Element das durch das Kapitel dargestellte <strong>Recordset</strong>-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="5205d-p101">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>. Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5205d-113">Aggregat</span><span class="sxs-lookup"><span data-stu-id="5205d-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="5205d-p102">Der Wert der Spalte wird abgeleitet durch Ausführen einer <em>Aggregatfunktion</em> für alle Zeilen oder eine Spalte aller Zeilen eines untergeordneten <strong>Recordset</strong>-Objekts. (Siehe "Aggregatfunktionen" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a>.)</span><span class="sxs-lookup"><span data-stu-id="5205d-p102">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>. (See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5205d-116">Berechneter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="5205d-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="5205d-p103">Der Wert der Spalte wird abgeleitet durch Berechnen eines Visual Basic für Applikationen-Ausdrucks für Spalten in der gleichen Zeile des <strong>Recordset</strong>-Objekts. Der Ausdruck ist das Argument für die CALC-Funktion. (Siehe "Berechneter Ausdruck" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a> und in <a href="visual-basic-for-applications-functions.md">Visual Basic für Applikationen (Funktionen)</a>.)</span><span class="sxs-lookup"><span data-stu-id="5205d-p103">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>. The expression is the argument to the CALC function. (See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5205d-120">Neu</span><span class="sxs-lookup"><span data-stu-id="5205d-120">new</span></span></p></td>
<td><p><span data-ttu-id="5205d-p104">Leere erstellte Felder, die später mit Daten aufgefüllt werden können. Die Spalte wird mit dem NEW-Schlüsselwort definiert. (Siehe "NEW-Schlüsselwort" im folgenden Thema, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregatfunktion, die CALC-Funktion und das NEW-Schlüsselwort</a>.)</span><span class="sxs-lookup"><span data-stu-id="5205d-p104">Empty, fabricated fields, which may be populated with data at a later time. The column is defined with the NEW keyword. (See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5205d-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span><span class="sxs-lookup"><span data-stu-id="5205d-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="5205d-p106">Sie können eine SQL JOIN-Klausel verwenden, um zwei Tabellen miteinander in Beziehung zu setzen. Durch ein hierarchisches **Recordset** -Objekt werden die Informationen jedoch möglicherweise effizienter dargestellt. In jeder Zeile eines durch JOIN erstellten **Recordset** -Objekts werden Informationen aus einer der Tabellen redundant wiederholt. Ein hierarchisches **Recordset** -Objekt hat nur ein übergeordnetes **Recordset** -Objekt für jedes einzelne mehrerer untergeordneter **Recordset** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="5205d-p106">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently. Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables. A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="5205d-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span><span class="sxs-lookup"><span data-stu-id="5205d-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

<span data-ttu-id="5205d-131">Shape commands can be nested.</span><span class="sxs-lookup"><span data-stu-id="5205d-131">Shape commands can be nested.</span></span> <span data-ttu-id="5205d-132">Das heißt, der *übergeordnete Befehl* oder *untergeordnete* Befehl kann selbst ein anderer Shape-Befehl sein.</span><span class="sxs-lookup"><span data-stu-id="5205d-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="5205d-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span><span class="sxs-lookup"><span data-stu-id="5205d-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="5205d-134">Weitere Informationen zum Navigieren in einem hierarchischen **Recordset** -Objekt finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="5205d-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="5205d-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="5205d-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5205d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5205d-136">See also</span></span>

- [<span data-ttu-id="5205d-137">Ausgeben von Befehlen an den zuGrunde liegenden Datenanbieter</span><span class="sxs-lookup"><span data-stu-id="5205d-137">Issuing Commands to the Underlying Data Provider</span></span>](issuing-commands-to-the-underlying-data-provider.md)

