---
title: Verwenden von parametrisierten Befehlen
TOCTitle: Operation of Parameterized Commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ae1b0545ac647b0034b0d24cac1a653cfeb4b7e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883848"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="48303-102">Verwenden von parametrisierten Befehlen</span><span class="sxs-lookup"><span data-stu-id="48303-102">Operation of Parameterized Commands</span></span>


<span data-ttu-id="48303-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48303-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48303-104">Wenn Sie ein umfangreiches untergeordnetes **Recordset** -Objekt verwenden, insbesondere im Vergleich zur Größe des übergeordneten **Recordset** -Objekts, aber nur auf ein paar untergeordnete Kapitel zugreifen müssen, könnte die Verwendung eines parametrisierten Befehls effizienter sein.</span><span class="sxs-lookup"><span data-stu-id="48303-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="48303-105">Einen *nicht parametrisierten Befehl* Ruft die gesamte über- und untergeordnete **Recordset-Objekte**, fügt eine Kapitelspalte an das übergeordnete Element und weist einen Verweis auf das zugehörige untergeordnete Kapitel für jede Zeile des übergeordneten.</span><span class="sxs-lookup"><span data-stu-id="48303-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="48303-106">Einen *parametrisierten Befehl* Ruft das gesamte übergeordnete **Recordset-Objekt**, sondern nur das Kapitel des **Recordset-Objekt** abgerufen, wenn auf die Kapitelspalte zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="48303-106">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed.</span></span> <span data-ttu-id="48303-107">Dieser Unterschied bei der Abrufstrategie kann erhebliche Leistungsvorteile bieten.</span><span class="sxs-lookup"><span data-stu-id="48303-107">This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="48303-108">Beispielsweise können Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="48303-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="48303-109">Die über- und untergeordneten Tabellen haben einen Spaltennamen in allgemeine, Cust\_Id *.*</span><span class="sxs-lookup"><span data-stu-id="48303-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="48303-110">Der *untergeordnete Befehl* weist Platzhalter "?" die Klausel verknüpfen bezieht (d. h., "... PARAMETER 0").</span><span class="sxs-lookup"><span data-stu-id="48303-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>


> [!NOTE]
> <P><span data-ttu-id="48303-p103">[!HINWEIS] Die PARAMETER-Klausel bezieht sich ausschließlich auf die SHAPE-Befehlssyntax. Sie ist weder dem <A href="parameter-object-ado.md">Parameter</A>-Objekt noch der <A href="parameters-collection-ado.md">Parameters</A>-Auflistung von ADO zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="48303-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO <A href="parameter-object-ado.md">Parameter</A> object or the <A href="parameters-collection-ado.md">Parameters</A> collection.</span></span></P>



<span data-ttu-id="48303-113">Wenn der parametrisierte SHAPE-Befehl ausgeführt wird, passiert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="48303-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="48303-114">Der übergeordnete Befehl wird ausgeführt und gibt ein übergeordnetes Recordset-Objekt aus der Customers-Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="48303-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="48303-115">Eine Kapitelspalte wird an das übergeordnete **Recordset** -Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="48303-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="48303-116">Wenn auf die Kapitelspalte einer übergeordneten Zeile zugegriffen wird, der *untergeordnete Befehl* wird ausgeführt, mit dem Wert der customer.cust\_Id als Wert des Parameters.</span><span class="sxs-lookup"><span data-stu-id="48303-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="48303-117">Alle Zeilen in der in Schritt 3 erstellte Anbieter Datenrowset dienen zum Auffüllen des untergeordneten **Recordset-Objekts**.</span><span class="sxs-lookup"><span data-stu-id="48303-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="48303-118">In diesem Beispiel wird, die alle Zeilen in der Orders-Tabelle, in dem die Cust\_Id gleich dem Wert der customer.cust\_Id.</span><span class="sxs-lookup"><span data-stu-id="48303-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="48303-119">Standardmäßig wird das untergeordnete **Recordset**s auf dem Client zwischengespeichert werden, bis alle Verweise auf das übergeordnete **Recordset** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="48303-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="48303-120">Wenn dieses Verhalten ändern möchten, legen Sie die **Recordset** - [dynamische Eigenschaft](ado-dynamic-property-index.md)**Cache untergeordneten Zeilen** auf **false festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="48303-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="48303-121">Ein Verweis auf die abgerufenen untergeordneten Zeilen (das heißt, das Kapitel des untergeordneten **Recordset**-Objekts) wird in der Kapitelspalte der aktuellen Zeile des übergeordneten **Recordset**-Objekts eingefügt.</span><span class="sxs-lookup"><span data-stu-id="48303-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="48303-122">Die Schritte 3 bis 5 werden wiederholt, wenn auf die Kapitelspalte einer anderen Zeile zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="48303-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="48303-p105">Die dynamische Eigenschaft **Cache Child Rows** wird standardmäßig auf **True** festgelegt. Das Zwischenspeicherungsverhalten hängt von den Parameterwerten der Abfrage ab. Bei einer Abfrage mit einem einzelnen Parameter wird das untergeordnete **Recordset** -Objekt für einen bestimmten Parameterwert zwischen den Anforderungen für ein untergeordnetes Element mit diesem Wert zwischengespeichert. Der folgende Code veranschaulicht dies:</span><span class="sxs-lookup"><span data-stu-id="48303-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

```vb 
 
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

<span data-ttu-id="48303-127">Bei einer Abfrage mit mehreren Parametern wird nur ein zwischengespeichertes untergeordnetes Element verwendet, wenn alle Parameterwerte den zwischengespeicherten Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="48303-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="48303-128">Parametrisierte Befehle und komplexe Beziehungen zwischen über- und untergeordneten Elementen</span><span class="sxs-lookup"><span data-stu-id="48303-128">Parameterized Commands and Complex Parent Child Relations</span></span>

<span data-ttu-id="48303-129">Zusätzlich zur Verwendung von parametrisierter Befehlen zum Verbessern der Leistung einer Equi-Join-Typ-Hierarchie, können parametrisierte Befehle zur Unterstützung von komplexerer über-und untergeordneten Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48303-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="48303-130">Angenommen, Sie verwenden eine Datenbank Little League mit zwei Tabellen: Basisplan, der die Teams (Team\_-Id, Team\_Name) und andere Spiele (Datum und private\_Team, besuchen\_Team).</span><span class="sxs-lookup"><span data-stu-id="48303-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="48303-131">Mit einer nicht parametrisierten Hierarchie können die Teams- und Spieletabellen nicht so miteinander verknüpft werden, dass das untergeordnete **Recordset** -Objekt für jedes Team den vollständigen Spielplan enthält.</span><span class="sxs-lookup"><span data-stu-id="48303-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="48303-132">Sie können Kapitel erstellen, die den Heimspielplan oder den Auswärtsspielplan enthalten, jedoch nicht beides.</span><span class="sxs-lookup"><span data-stu-id="48303-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="48303-133">Denn die RELATE-Klausel beschränkt Sie auf Beziehungen zwischen über- und untergeordneten Elementen im Format (pc1=cc1) AND (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="48303-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="48303-134">Dies, wenn der Befehl enthielt "verknüpfen Team\_Id zu Hause\_Team, Team\_Id zu besuchen\_Team", erhalten Sie nur spielen, wurde ein Team selbst wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="48303-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="48303-135">Verfügbare ist "(Team\_Id = home\_Team) oder (Team\_Id = Vorsichtsmaßnahmen\_Team)", aber der Shape-Anbieter Momentaufnahmen nicht unterstützt die OR-Klausel.</span><span class="sxs-lookup"><span data-stu-id="48303-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="48303-p108">Sie können einen parametrisierten Befehl verwenden, um das gewünschte Ergebnis zu erhalten. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="48303-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="48303-138">Dieses Beispiel nutzt die größere Flexibilität der WHERE-Klausel von SQL, um das gewünschte Ergebnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="48303-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

