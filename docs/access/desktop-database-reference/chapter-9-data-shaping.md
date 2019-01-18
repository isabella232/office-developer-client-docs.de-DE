---
title: 'Kapitel 9: Daten modellieren'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721554"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="65546-102">Kapitel 9: Daten modellieren</span><span class="sxs-lookup"><span data-stu-id="65546-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="65546-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65546-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65546-104">*Data shaping* bietet eine Möglichkeit zum Abfragen einer Datenquelle und Zurückgeben einer [Recordset-Objekt](recordset-object-ado.md) , das eine hierarchische Beziehung zwischen zwei oder mehr logische Entitäten (einer Hierarchie) darstellt.</span><span class="sxs-lookup"><span data-stu-id="65546-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="65546-105">Ein klassisches Beispiel für eine hierarchische Beziehung sind Kunden und Aufträge.</span><span class="sxs-lookup"><span data-stu-id="65546-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="65546-106">Für jeden Kunden in einer Datenbank können null oder mehr Aufträge vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="65546-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="65546-107">Mit regulären SQL-Befehlen könnten die Daten mithilfe der JOIN-Syntax abgerufen werden, was jedoch ineffizient und unhandlich sein kann, da in jedem für eine bestimmte Übergeordnet-Untergeordnet-Beziehung zurückgegebenen Datensatz redundante Daten zum übergeordneten Element wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="65546-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="65546-108">Durch Datenstrukturierung kann ein einzelner übergeordneter Datensatz im übergeordneten **Recordset** in Beziehung zu mehreren untergeordneten Datensätzen im **Recordset** gesetzt werden, wodurch die Redundanz von JOIN vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="65546-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="65546-109">Die meisten Personen finden das Programmiermodell mit Übergeordnet-Untergeordnet-Beziehungen und mehreren **Recordsets** natürlicher und meinen, dass sie mit ihm einfacher arbeiten als mit dem JOIN-Modell und einem einzelnen **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="65546-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="65546-p102">Die Datenstrukturierungssyntax stellt außerdem weitere Funktionen bereit. Entwickler können neue **Recordset** -Objekte ohne zugrunde liegende Datenquelle erstellen, indem sie das NEW-Schlüsselwort verwenden, um die Felder der über- und untergeordneten **Recordsets** zu beschreiben. Das neue **Recordset** -Objekt kann mit Daten aufgefüllt und permanent gespeichert werden. Entwickler können außerdem verschiedene Berechnungen oder Aggregationen (z. B. SUM, AVG und MAX) für untergeordnete Felder ausführen. Mit Datenstrukturierung kann auch ein übergeordnetes **Recordset** aus einem untergeordneten **Recordset** erstellt werden, indem Datensätze im untergeordneten Element gruppiert werden und im übergeordneten Element für jede Gruppe im untergeordneten Element eine Zeile platziert wird.</span><span class="sxs-lookup"><span data-stu-id="65546-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="65546-115">Weitere Informationen zur Datenstrukturierung finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="65546-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="65546-116">Erforderliche Anbieter für Datenmodellierung</span><span class="sxs-lookup"><span data-stu-id="65546-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="65546-117">Shape Compute-Klausel</span><span class="sxs-lookup"><span data-stu-id="65546-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="65546-118">Fabrizieren hierarchischer Recordsets</span><span class="sxs-lookup"><span data-stu-id="65546-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="65546-119">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="65546-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="65546-120">Formal Shape Grammar</span><span class="sxs-lookup"><span data-stu-id="65546-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="65546-121">Funktionen (Visual Basic for Applications)</span><span class="sxs-lookup"><span data-stu-id="65546-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="65546-122">Shape Append-Klausel (ADO)</span><span class="sxs-lookup"><span data-stu-id="65546-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="65546-123">Datenstrukturierung (ADO)</span><span class="sxs-lookup"><span data-stu-id="65546-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="65546-124">Shape-Befehle im Allgemeinen (ADO)</span><span class="sxs-lookup"><span data-stu-id="65546-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

