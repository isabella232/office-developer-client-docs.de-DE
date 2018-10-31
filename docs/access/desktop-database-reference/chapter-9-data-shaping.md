---
title: 'Kapitel 9: Daten modellieren'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4636c853f58557b30474b78d902131329084a1a2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863885"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="a2a55-102">Kapitel 9: Daten modellieren</span><span class="sxs-lookup"><span data-stu-id="a2a55-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="a2a55-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2a55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a2a55-104">*Data shaping* bietet eine Möglichkeit zum Abfragen einer Datenquelle und Zurückgeben einer [Recordset-Objekt](recordset-object-ado.md) , das eine hierarchische Beziehung zwischen zwei oder mehr logische Entitäten (einer Hierarchie) darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2a55-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="a2a55-105">Ein klassisches Beispiel für eine hierarchische Beziehung sind Kunden und Aufträge.</span><span class="sxs-lookup"><span data-stu-id="a2a55-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="a2a55-106">Für jeden Kunden in einer Datenbank können null oder mehr Aufträge vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a2a55-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="a2a55-107">Mit regulären SQL-Befehlen könnten die Daten mithilfe der JOIN-Syntax abgerufen werden, was jedoch ineffizient und unhandlich sein kann, da in jedem für eine bestimmte Übergeordnet-Untergeordnet-Beziehung zurückgegebenen Datensatz redundante Daten zum übergeordneten Element wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="a2a55-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="a2a55-108">Durch Datenstrukturierung kann ein einzelner übergeordneter Datensatz im übergeordneten **Recordset** in Beziehung zu mehreren untergeordneten Datensätzen im **Recordset** gesetzt werden, wodurch die Redundanz von JOIN vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="a2a55-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="a2a55-109">Die meisten Personen finden das Programmiermodell mit Übergeordnet-Untergeordnet-Beziehungen und mehreren **Recordsets** natürlicher und meinen, dass sie mit ihm einfacher arbeiten als mit dem JOIN-Modell und einem einzelnen **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a2a55-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="a2a55-p102">Die Datenstrukturierungssyntax stellt außerdem weitere Funktionen bereit. Entwickler können neue **Recordset** -Objekte ohne zugrunde liegende Datenquelle erstellen, indem sie das NEW-Schlüsselwort verwenden, um die Felder der über- und untergeordneten **Recordsets** zu beschreiben. Das neue **Recordset** -Objekt kann mit Daten aufgefüllt und permanent gespeichert werden. Entwickler können außerdem verschiedene Berechnungen oder Aggregationen (z. B. SUM, AVG und MAX) für untergeordnete Felder ausführen. Mit Datenstrukturierung kann auch ein übergeordnetes **Recordset** aus einem untergeordneten **Recordset** erstellt werden, indem Datensätze im untergeordneten Element gruppiert werden und im übergeordneten Element für jede Gruppe im untergeordneten Element eine Zeile platziert wird.</span><span class="sxs-lookup"><span data-stu-id="a2a55-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="a2a55-115">Weitere Informationen zur Datenstrukturierung finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a2a55-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="a2a55-116">Erforderliche Anbieter für die Datenstrukturierung</span><span class="sxs-lookup"><span data-stu-id="a2a55-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="a2a55-117">Shape Compute-Klausel</span><span class="sxs-lookup"><span data-stu-id="a2a55-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="a2a55-118">Erstellen hierarchischer Recordsets</span><span class="sxs-lookup"><span data-stu-id="a2a55-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="a2a55-119">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="a2a55-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="a2a55-120">Formale Grammatik für Formen</span><span class="sxs-lookup"><span data-stu-id="a2a55-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="a2a55-121">Visual Basic für Applikationen (Funktionen)</span><span class="sxs-lookup"><span data-stu-id="a2a55-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="a2a55-122">Shape Append Clause (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2a55-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="a2a55-123">Datenstrukturierung (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2a55-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="a2a55-124">Shape Commands in General (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2a55-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

