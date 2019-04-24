---
title: Shape Compute-Klausel
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306454"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="03bc7-102">Shape Compute-Klausel</span><span class="sxs-lookup"><span data-stu-id="03bc7-102">Shape Compute clause</span></span>

<span data-ttu-id="03bc7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03bc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03bc7-104">Durch eine COMPUTE-Klausel für Formen wird ein übergeordnetes **Recordset**-Objekt generiert, dessen Spalten aus Folgendem bestehen: aus einem Verweis auf das untergeordnete **Recordset**-Objekt; aus optionalen Spalten, deren Inhalt ein Kapitel, neue oder berechnete Spalten oder das Ergebnis der Ausführung von Aggregatfunktionen für das untergeordnete **Recordset**-Objekt oder ein vorher geformtes **Recordset**-Objekt sein kann; und aus allen Spalten des untergeordneten **Recordset**-Objekts, die in der optionalen BY-Klausel aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="03bc7-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03bc7-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="03bc7-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03bc7-106">Description</span></span>

<span data-ttu-id="03bc7-107">Die Teile dieser Klausel lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="03bc7-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="03bc7-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="03bc7-108">*child-command*</span></span>

  - <span data-ttu-id="03bc7-109">Besteht aus einem der Folgenden:</span><span class="sxs-lookup"><span data-stu-id="03bc7-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="03bc7-p101">Ein Abfragebefehl in geschweiften Klammern ("{}"), der ein untergeordnetes **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenanbieter ausgegeben, und die Syntax des Befehls hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="03bc7-113">Der Name eines vorhandenen geformten **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="03bc7-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="03bc7-114">Ein weiterer Shape-Befehl.</span><span class="sxs-lookup"><span data-stu-id="03bc7-114">Another shape command.</span></span>
    
    - <span data-ttu-id="03bc7-115">Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.</span><span class="sxs-lookup"><span data-stu-id="03bc7-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="03bc7-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="03bc7-116">*child-alias*</span></span>

  - <span data-ttu-id="03bc7-p102">Ein Alias, mit dem auf das **Recordset**-Objekt verwiesen wird, das von *child-command* zurückgegeben wird. *child-alias* ist in der Liste der Spalten in der COMPUTE-Klausel erforderlich und definiert die Beziehung zwischen den übergeordneten und untergeordneten **Recordset**-Objekten.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p102">An alias used to refer to the **Recordset** returned by the *child-command.* The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="03bc7-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="03bc7-119">*appended-column-list*</span></span>

  - <span data-ttu-id="03bc7-p103">Eine Liste, in der durch jedes Element eine Spalte im generierten übergeordneten Element definiert wird. Jedes Element enthält eine Kapitelspalte, eine neue Spalte, eine berechnete Spalte oder einen Wert, der das Ergebnis einer Aggregatfunktion für das untergeordnete **Recordset** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="03bc7-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="03bc7-122">*grp-field-list*</span></span>

  - <span data-ttu-id="03bc7-123">Eine Liste der Spalten in den übergeordneten und untergeordneten **Recordset**-Objekten, durch die angegeben wird, wie die Zeilen im untergeordneten Objekt gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03bc7-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="03bc7-124">Für jede Spalte in *grp-field-list* ist in den untergeordneten und übergeordneten **Recordset**-Objekten eine entsprechende Spalte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="03bc7-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="03bc7-125">Für jede Zeile im übergeordneten **Recordset**-Objekt enthalten die Spalten von *grp-field-list* eindeutige Werte, und das **Recordset**-Objekt, auf das von der übergeordneten Zeile verwiesen wird, besteht ausschließlich aus untergeordneten Zeilen, deren *grp-field-list*-Spalten die gleichen Werte enthalten wie die übergeordnete Zeile.</span><span class="sxs-lookup"><span data-stu-id="03bc7-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="03bc7-p105">Wenn die BY-Klausel enthalten ist, werden die Zeilen des untergeordneten **Recordset**-Objekts basierend auf den Spalten in der COMPUTE-Klausel gruppiert. Das übergeordnete **Recordset**-Objekt enthält eine Zeile für jede Zeilengruppe im untergeordneten **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="03bc7-p106">Wenn die BY-Klausel weggelassen wird, wird das gesamte untergeordnete **Recordset** -Objekt als einzelne Gruppe behandelt, und das übergeordnete **Recordset** -Objekt enthält genau eine Zeile. Durch diese Zeile wird auf das gesamte untergeordnete **Recordset** -Objekt verwiesen. Durch Weglassen der BY-Klausel können Sie "Gesamtsummenaggregate" für das gesamte untergeordnete **Recordset** -Objekt berechnen.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="03bc7-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="03bc7-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="03bc7-p107">Unabhängig davon, auf welche Weise das übergeordnete **Recordset**-Objekt geformt wird (mithilfe von COMPUTE oder mithilfe von APPEND), enthält es eine Kapitelspalte, die verwendet wird, um es in Beziehung zu einem untergeordneten **Recordset**-Objekt zu setzen. Wenn Sie dies möchten, kann das übergeordnete **Recordset**-Objekt auch Spalten enthalten, die Aggregate (SUM, MIN, MAX usw.) für die untergeordneten Zeilen enthalten. Sowohl das übergeordnete als auch das untergeordnete **Recordset**-Objekt können Spalten enthalten, die einen Ausdruck für die Zeile im **Recordset**-Objekt enthalten, sowie Spalten, die neu und anfangs leer sind.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="03bc7-135">Vorgang</span><span class="sxs-lookup"><span data-stu-id="03bc7-135">Operation</span></span>

<span data-ttu-id="03bc7-136">*child-command* wird an den Anbieter ausgegeben, von dem ein untergeordnetes **Recordset**-Objekt zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03bc7-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="03bc7-p108">Durch die COMPUTE-Klausel werden die Spalten des übergeordneten **Recordset**-Objekts angegeben, bei dem es sich um einen Verweis auf das untergeordnete **Recordset**-Objekt, auf eines oder mehrere Aggregate, auf einen berechneten Ausdruck oder auf neue Spalten handeln kann. Wenn eine BY-Klausel vorhanden ist, werden die dadurch definierten Spalten ebenfalls dem übergeordneten **Recordset**-Objekt angefügt. Durch die BY-Klausel wird angegeben, wie die Zeilen des untergeordneten **Recordset**-Objekts gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="03bc7-140">Nehmen wir z. B. an, Sie haben eine Tabelle namens Demografische Daten, die aus den Feldern Bundesland, Ort und Bevölkerung besteht (die Bevölkerungszahlen dienen ausschließlich der Veranschaulichung).</span><span class="sxs-lookup"><span data-stu-id="03bc7-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03bc7-141">Status</span><span class="sxs-lookup"><span data-stu-id="03bc7-141">State</span></span></p></th>
<th><p><span data-ttu-id="03bc7-142">Stadt</span><span class="sxs-lookup"><span data-stu-id="03bc7-142">City</span></span></p></th>
<th><p><span data-ttu-id="03bc7-143">Grundgesamtheit</span><span class="sxs-lookup"><span data-stu-id="03bc7-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-144">WA</span><span class="sxs-lookup"><span data-stu-id="03bc7-144">WA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="03bc7-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="03bc7-146">700.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-147">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-147">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-148">Medford</span><span class="sxs-lookup"><span data-stu-id="03bc7-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="03bc7-149">200.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-150">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-150">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-151">Portland</span><span class="sxs-lookup"><span data-stu-id="03bc7-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="03bc7-152">400,000</span><span class="sxs-lookup"><span data-stu-id="03bc7-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-153">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="03bc7-153">CA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-154">München</span><span class="sxs-lookup"><span data-stu-id="03bc7-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="03bc7-155">800.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-156">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="03bc7-156">CA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-157">Nürnberg</span><span class="sxs-lookup"><span data-stu-id="03bc7-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="03bc7-158">600.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-159">WA</span><span class="sxs-lookup"><span data-stu-id="03bc7-159">WA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="03bc7-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="03bc7-161">500.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-162">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-162">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="03bc7-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="03bc7-164">300,000</span><span class="sxs-lookup"><span data-stu-id="03bc7-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03bc7-165">Geben Sie nun diesen Shape-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="03bc7-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="03bc7-166">Durch diesen Befehl wird ein geformtes **Recordset** -Objekt mit zwei Ebenen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="03bc7-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="03bc7-167">Die übergeordnete Ebene ist ein generiertes **Recordset** mit einer Aggregat Spalte (Sum (Rs. Population)), eine Spalte, die auf das untergeordnete **Recordset** (RS) verweist, und eine Spalte zum Gruppieren des untergeordneten **Recordsets** (Status).</span><span class="sxs-lookup"><span data-stu-id="03bc7-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="03bc7-168">Die untergeordnete Ebene ist das vom Abfragebefehl () zurückgegebene **Recordset** (), eine Spalte, die auf das untergeordnete **Recordset** (RS) verweist, und eine Spalte zum Gruppieren des untergeordneten **Recordsets** (Status).</span><span class="sxs-lookup"><span data-stu-id="03bc7-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="03bc7-169">Die untergeordnete Ebene ist das vom Abfragebefehl zurückgegebene **Recordset** (Wählen Sie \* aus Demographie aus).</span><span class="sxs-lookup"><span data-stu-id="03bc7-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="03bc7-p110">Die Detailzeilen des untergeordneten **Recordset** -Objekts werden nach Bundesland, aber ansonsten ohne besondere Reihenfolge gruppiert. Das heißt, die Gruppen befinden sich nicht in einer alphabetischen oder numerischen Reihenfolge. Wenn das übergeordnete **Recordset** -Objekt sortiert werden soll, können Sie die **Sort** -Methode für das **Recordset** -Objekt zum Sortieren des übergeordneten **Recordset** -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="03bc7-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="03bc7-p111">Sie können jetzt im geöffneten übergeordneten **Recordset** -Objekt navigieren und auf die untergeordneten **Recordset** -Detailobjekte zugreifen. Weitere Informationen finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="03bc7-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="03bc7-175">**Übergeordnete und untergeordnete Detailergebnisdatensätze**</span><span class="sxs-lookup"><span data-stu-id="03bc7-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="03bc7-176">**Übergeordnet**</span><span class="sxs-lookup"><span data-stu-id="03bc7-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03bc7-177">SUM (Rs. Grundgesamtheit</span><span class="sxs-lookup"><span data-stu-id="03bc7-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="03bc7-178">RS</span><span class="sxs-lookup"><span data-stu-id="03bc7-178">rs</span></span></p></th>
<th><p><span data-ttu-id="03bc7-179">Status</span><span class="sxs-lookup"><span data-stu-id="03bc7-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-180">1,3 Millionen</span><span class="sxs-lookup"><span data-stu-id="03bc7-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="03bc7-181">Verweis auf child1</span><span class="sxs-lookup"><span data-stu-id="03bc7-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="03bc7-182">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="03bc7-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-183">1,2 Millionen</span><span class="sxs-lookup"><span data-stu-id="03bc7-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="03bc7-184">Verweis auf child2</span><span class="sxs-lookup"><span data-stu-id="03bc7-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="03bc7-185">WA</span><span class="sxs-lookup"><span data-stu-id="03bc7-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-186">1,1 Millionen</span><span class="sxs-lookup"><span data-stu-id="03bc7-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="03bc7-187">Verweis auf Child3</span><span class="sxs-lookup"><span data-stu-id="03bc7-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="03bc7-188">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03bc7-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="03bc7-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03bc7-190">Status</span><span class="sxs-lookup"><span data-stu-id="03bc7-190">State</span></span></p></th>
<th><p><span data-ttu-id="03bc7-191">Stadt</span><span class="sxs-lookup"><span data-stu-id="03bc7-191">City</span></span></p></th>
<th><p><span data-ttu-id="03bc7-192">Grundgesamtheit</span><span class="sxs-lookup"><span data-stu-id="03bc7-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-193">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="03bc7-193">CA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-194">München</span><span class="sxs-lookup"><span data-stu-id="03bc7-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="03bc7-195">800.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-196">Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="03bc7-196">CA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-197">Nürnberg</span><span class="sxs-lookup"><span data-stu-id="03bc7-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="03bc7-198">600.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03bc7-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="03bc7-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03bc7-200">Status</span><span class="sxs-lookup"><span data-stu-id="03bc7-200">State</span></span></p></th>
<th><p><span data-ttu-id="03bc7-201">Stadt</span><span class="sxs-lookup"><span data-stu-id="03bc7-201">City</span></span></p></th>
<th><p><span data-ttu-id="03bc7-202">Grundgesamtheit</span><span class="sxs-lookup"><span data-stu-id="03bc7-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-203">WA</span><span class="sxs-lookup"><span data-stu-id="03bc7-203">WA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="03bc7-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="03bc7-205">700.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-206">WA</span><span class="sxs-lookup"><span data-stu-id="03bc7-206">WA</span></span></p></td>
<td><p><span data-ttu-id="03bc7-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="03bc7-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="03bc7-208">500.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03bc7-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="03bc7-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03bc7-210">Status</span><span class="sxs-lookup"><span data-stu-id="03bc7-210">State</span></span></p></th>
<th><p><span data-ttu-id="03bc7-211">Stadt</span><span class="sxs-lookup"><span data-stu-id="03bc7-211">City</span></span></p></th>
<th><p><span data-ttu-id="03bc7-212">Grundgesamtheit</span><span class="sxs-lookup"><span data-stu-id="03bc7-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-213">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-213">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-214">Medford</span><span class="sxs-lookup"><span data-stu-id="03bc7-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="03bc7-215">200.000</span><span class="sxs-lookup"><span data-stu-id="03bc7-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03bc7-216">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-216">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-217">Portland</span><span class="sxs-lookup"><span data-stu-id="03bc7-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="03bc7-218">400,000</span><span class="sxs-lookup"><span data-stu-id="03bc7-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03bc7-219">ODER</span><span class="sxs-lookup"><span data-stu-id="03bc7-219">OR</span></span></p></td>
<td><p><span data-ttu-id="03bc7-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="03bc7-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="03bc7-221">300,000</span><span class="sxs-lookup"><span data-stu-id="03bc7-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

