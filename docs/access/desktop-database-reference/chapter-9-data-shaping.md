---
title: 'Kapitel 9: Datenstrukturierung'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8217be1004ea8304501e7d32908b8af269873b7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475168"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="7e7fb-102">Kapitel 9: Datenstrukturierung</span><span class="sxs-lookup"><span data-stu-id="7e7fb-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="7e7fb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e7fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e7fb-104">*Data shaping* bietet eine Möglichkeit zum Abfragen einer Datenquelle und Zurückgeben einer [Recordset-Objekt](recordset-object-ado.md) , das eine hierarchische Beziehung zwischen zwei oder mehr logische Entitäten (einer Hierarchie) darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="7e7fb-105">Ein klassisches Beispiel für eine hierarchische Beziehung sind Kunden und Aufträge.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="7e7fb-106">Für jeden Kunden in einer Datenbank können null oder mehr Aufträge vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="7e7fb-107">Mit regulären SQL-Befehlen könnten die Daten mithilfe der JOIN-Syntax abgerufen werden, was jedoch ineffizient und unhandlich sein kann, da in jedem für eine bestimmte Übergeordnet-Untergeordnet-Beziehung zurückgegebenen Datensatz redundante Daten zum übergeordneten Element wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="7e7fb-108">Durch Datenstrukturierung kann ein einzelner übergeordneter Datensatz im übergeordneten **Recordset** in Beziehung zu mehreren untergeordneten Datensätzen im **Recordset** gesetzt werden, wodurch die Redundanz von JOIN vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="7e7fb-109">Die meisten Personen finden das Programmiermodell mit Übergeordnet-Untergeordnet-Beziehungen und mehreren **Recordsets** natürlicher und meinen, dass sie mit ihm einfacher arbeiten als mit dem JOIN-Modell und einem einzelnen **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="7e7fb-p102">Die Datenstrukturierungssyntax stellt außerdem weitere Funktionen bereit. Entwickler können neue **Recordset** -Objekte ohne zugrunde liegende Datenquelle erstellen, indem sie das NEW-Schlüsselwort verwenden, um die Felder der über- und untergeordneten **Recordsets** zu beschreiben. Das neue **Recordset** -Objekt kann mit Daten aufgefüllt und permanent gespeichert werden. Entwickler können außerdem verschiedene Berechnungen oder Aggregationen (z. B. SUM, AVG und MAX) für untergeordnete Felder ausführen. Mit Datenstrukturierung kann auch ein übergeordnetes **Recordset** aus einem untergeordneten **Recordset** erstellt werden, indem Datensätze im untergeordneten Element gruppiert werden und im übergeordneten Element für jede Gruppe im untergeordneten Element eine Zeile platziert wird.</span><span class="sxs-lookup"><span data-stu-id="7e7fb-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="7e7fb-115">Weitere Informationen zur Datenstrukturierung finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7e7fb-115">See the following topics to learn more about data shaping:</span></span>

  - [<span data-ttu-id="7e7fb-116">Datenstrukturierung (Zusammenfassung)</span><span class="sxs-lookup"><span data-stu-id="7e7fb-116">Data Shaping Summary</span></span>](data-shaping-summary.md)

  - [<span data-ttu-id="7e7fb-117">Erforderliche Anbieter für die Datenstrukturierung</span><span class="sxs-lookup"><span data-stu-id="7e7fb-117">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

  - [<span data-ttu-id="7e7fb-118">Shape-Befehle im Allgemeinen</span><span class="sxs-lookup"><span data-stu-id="7e7fb-118">Shape Commands in General</span></span>](shape-commands-in-general.md)

  - [<span data-ttu-id="7e7fb-119">APPEND-Klausel für Formen</span><span class="sxs-lookup"><span data-stu-id="7e7fb-119">Shape APPEND Clause</span></span>](shape-append-clause.md)

  - [<span data-ttu-id="7e7fb-120">COMPUTE-Klausel für Formen</span><span class="sxs-lookup"><span data-stu-id="7e7fb-120">Shape COMPUTE Clause</span></span>](shape-compute-clause.md)

  - [<span data-ttu-id="7e7fb-121">Erstellen hierarchischer Recordsets</span><span class="sxs-lookup"><span data-stu-id="7e7fb-121">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

  - [<span data-ttu-id="7e7fb-122">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="7e7fb-122">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

  - [<span data-ttu-id="7e7fb-123">Formale Grammatik für Formen</span><span class="sxs-lookup"><span data-stu-id="7e7fb-123">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

  - [<span data-ttu-id="7e7fb-124">Visual Basic für Applikationen (Funktionen)</span><span class="sxs-lookup"><span data-stu-id="7e7fb-124">Visual Basic for Applications Functions</span></span>](visual-basic-for-applications-functions.md)

