---
title: Compute-Klausel für Formen
TOCTitle: Shape Compute Clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e35cfc7bc5df144fa1938f794cb705bf2f1448c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889931"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="3edc3-102">Compute-Klausel für Formen</span><span class="sxs-lookup"><span data-stu-id="3edc3-102">Shape Compute Clause</span></span>

<span data-ttu-id="3edc3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3edc3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3edc3-104">Durch eine COMPUTE-Klausel für Formen wird ein übergeordnetes **Recordset** -Objekt generiert, dessen Spalten aus Folgendem bestehen: aus einem Verweis auf das untergeordnete **Recordset** -Objekt; aus optionalen Spalten, deren Inhalt ein Kapitel, neue oder berechnete Spalten oder das Ergebnis der Ausführung von Aggregatfunktionen für das untergeordnete **Recordset** -Objekt oder ein vorher geformtes **Recordset** -Objekt sein kann; und aus allen Spalten des untergeordneten **Recordset** -Objekts, die in der optionalen BY-Klausel aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3edc3-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="3edc3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3edc3-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="3edc3-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3edc3-106">Description</span></span>

<span data-ttu-id="3edc3-107">Die Teile dieser Klausel lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3edc3-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="3edc3-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="3edc3-108">*child-command*</span></span>

  - <span data-ttu-id="3edc3-109">Besteht aus einem der Folgenden:</span><span class="sxs-lookup"><span data-stu-id="3edc3-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="3edc3-p101">Ein Abfragebefehl in geschweiften Klammern ("{}"), der ein untergeordnetes **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenanbieter ausgegeben, und die Syntax des Befehls hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="3edc3-113">Der Name eines vorhandenen geformten **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3edc3-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="3edc3-114">Ein weiterer Shape-Befehl.</span><span class="sxs-lookup"><span data-stu-id="3edc3-114">Another shape command.</span></span>
    
    - <span data-ttu-id="3edc3-115">Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.</span><span class="sxs-lookup"><span data-stu-id="3edc3-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="3edc3-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="3edc3-116">*child-alias*</span></span>

  - <span data-ttu-id="3edc3-117">Ein Alias verwendet, um an das **Recordset-Objekt** verweisen zurückgegebene der *untergeordnete Befehl.*</span><span class="sxs-lookup"><span data-stu-id="3edc3-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="3edc3-118">Der *Alias des untergeordneten Elements* in der Liste der Spalten in der COMPUTE-Klausel ist erforderlich, und definiert die Beziehung zwischen über- und untergeordnete **Recordset** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="3edc3-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="3edc3-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="3edc3-119">*appended-column-list*</span></span>

  - <span data-ttu-id="3edc3-p103">Eine Liste, in der durch jedes Element eine Spalte im generierten übergeordneten Element definiert wird. Jedes Element enthält eine Kapitelspalte, eine neue Spalte, eine berechnete Spalte oder einen Wert, der das Ergebnis einer Aggregatfunktion für das untergeordnete **Recordset** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="3edc3-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="3edc3-122">*grp-field-list*</span></span>

  - <span data-ttu-id="3edc3-123">Eine Liste der Spalten in den übergeordneten und untergeordneten **Recordset** -Objekten, durch die angegeben wird, wie die Zeilen im untergeordneten Objekt gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3edc3-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="3edc3-124">Für jede Spalte in der *Gruppe-Feld-Liste* vorhanden ist eine entsprechende Spalte in der untergeordneten und übergeordneten **Recordset** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="3edc3-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="3edc3-125">Für jede Zeile im übergeordneten **Recordset-Objekts**, die *Gruppe Feldliste* Spalten eindeutige Werte haben und das untergeordnete **Recordset-Objekt** von der übergeordneten Zeile verwiesen, ausschließlich aus untergeordneten besteht Zeilen, deren *Gruppe Feldliste* Spalten enthalten dieselben Werte wie die übergeordneten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3edc3-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="3edc3-p105">Wenn die BY-Klausel enthalten ist, werden die Zeilen des untergeordneten **Recordset**-Objekts basierend auf den Spalten in der COMPUTE-Klausel gruppiert. Das übergeordnete **Recordset**-Objekt enthält eine Zeile für jede Zeilengruppe im untergeordneten **Recordset**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="3edc3-p106">Wenn die BY-Klausel weggelassen wird, wird das gesamte untergeordnete **Recordset** -Objekt als einzelne Gruppe behandelt, und das übergeordnete **Recordset** -Objekt enthält genau eine Zeile. Durch diese Zeile wird auf das gesamte untergeordnete **Recordset** -Objekt verwiesen. Durch Weglassen der BY-Klausel können Sie "Gesamtsummenaggregate" für das gesamte untergeordnete **Recordset** -Objekt berechnen.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="3edc3-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3edc3-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="3edc3-p107">Unabhängig davon, auf welche Weise das übergeordnete **Recordset** -Objekt geformt wird (mithilfe von COMPUTE oder mithilfe von APPEND), enthält es eine Kapitelspalte, die verwendet wird, um es in Beziehung zu einem untergeordneten **Recordset** -Objekt zu setzen. Wenn Sie dies möchten, kann das übergeordnete **Recordset** -Objekt auch Spalten enthalten, die Aggregate (SUM, MIN, MAX usw.) für die untergeordneten Zeilen enthalten. Sowohl das übergeordnete als auch das untergeordnete **Recordset** -Objekt können Spalten enthalten, die einen Ausdruck für die Zeile im **Recordset** -Objekt enthalten, sowie Spalten, die neu und anfangs leer sind.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="3edc3-135">Verwendung</span><span class="sxs-lookup"><span data-stu-id="3edc3-135">Operation</span></span>

<span data-ttu-id="3edc3-136">Der *untergeordnete Befehl* wird an den Anbieter ausgegeben, von dem ein untergeordnetes **Recordset-Objekt**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3edc3-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="3edc3-p108">Durch die COMPUTE-Klausel werden die Spalten des übergeordneten **Recordset** -Objekts angegeben, bei dem es sich um einen Verweis auf das untergeordnete **Recordset** -Objekt, auf eines oder mehrere Aggregate, auf einen berechneten Ausdruck oder auf neue Spalten handeln kann. Wenn eine BY-Klausel vorhanden ist, werden die dadurch definierten Spalten ebenfalls dem übergeordneten **Recordset** -Objekt angefügt. Durch die BY-Klausel wird angegeben, wie die Zeilen des untergeordneten **Recordset** -Objekts gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="3edc3-140">Nehmen wir z. B. an, Sie haben eine Tabelle namens Demografische Daten, die aus den Feldern Bundesland, Ort und Bevölkerung besteht (die Bevölkerungszahlen dienen ausschließlich der Veranschaulichung).</span><span class="sxs-lookup"><span data-stu-id="3edc3-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edc3-141">Bundesland</span><span class="sxs-lookup"><span data-stu-id="3edc3-141">State</span></span></p></th>
<th><p><span data-ttu-id="3edc3-142">Ort</span><span class="sxs-lookup"><span data-stu-id="3edc3-142">City</span></span></p></th>
<th><p><span data-ttu-id="3edc3-143">Bevölkerung</span><span class="sxs-lookup"><span data-stu-id="3edc3-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-144">Hessen</span><span class="sxs-lookup"><span data-stu-id="3edc3-144">WA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-145">Frankfurt</span><span class="sxs-lookup"><span data-stu-id="3edc3-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="3edc3-146">700.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-147">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-147">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-148">Köln</span><span class="sxs-lookup"><span data-stu-id="3edc3-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="3edc3-149">200.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-150">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-150">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-151">Düsseldorf</span><span class="sxs-lookup"><span data-stu-id="3edc3-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="3edc3-152">400.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-153">Bayern</span><span class="sxs-lookup"><span data-stu-id="3edc3-153">CA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-154">München</span><span class="sxs-lookup"><span data-stu-id="3edc3-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="3edc3-155">Um 800.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-156">Bayern</span><span class="sxs-lookup"><span data-stu-id="3edc3-156">CA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-157">Nürnberg</span><span class="sxs-lookup"><span data-stu-id="3edc3-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="3edc3-158">600.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-159">Hessen</span><span class="sxs-lookup"><span data-stu-id="3edc3-159">WA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-160">Offenbach</span><span class="sxs-lookup"><span data-stu-id="3edc3-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="3edc3-161">500.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-162">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-162">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-163">Dortmund</span><span class="sxs-lookup"><span data-stu-id="3edc3-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="3edc3-164">300.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3edc3-165">Geben Sie nun diesen Shape-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="3edc3-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="3edc3-166">Durch diesen Befehl wird ein geformtes **Recordset** -Objekt mit zwei Ebenen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3edc3-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="3edc3-167">Die übergeordnete Ebene ist ein generierten **Recordset-Objekt** mit einer Aggregatspalte (SUM(rs.population)), eine Spalte verweisen auf das untergeordnete **Recordset-Objekt** (Rs) und eine Spalte zum Gruppieren des untergeordneten **Recordset-Objekt** (Zustand).</span><span class="sxs-lookup"><span data-stu-id="3edc3-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="3edc3-168">Die untergeordneten Ebene ist das **Recordset-Objekt** durch den Befehl (Abfrage), eine Spalte verweisen auf das untergeordnete **Recordset-Objekt** (Rs) und eine Spalte zum Gruppieren des untergeordneten **Recordset-Objekt** (Zustand) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3edc3-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="3edc3-169">Die untergeordneten Ebene ist das **Recordset-Objekt** durch den Abfragebefehl zurückgegebenen (Wählen Sie \* aus demografischer).</span><span class="sxs-lookup"><span data-stu-id="3edc3-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="3edc3-p110">Die Detailzeilen des untergeordneten **Recordset** -Objekts werden nach Bundesland, aber ansonsten ohne besondere Reihenfolge gruppiert. Das heißt, die Gruppen befinden sich nicht in einer alphabetischen oder numerischen Reihenfolge. Wenn das übergeordnete **Recordset** -Objekt sortiert werden soll, können Sie die **Sort** -Methode für das **Recordset** -Objekt zum Sortieren des übergeordneten **Recordset** -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="3edc3-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="3edc3-p111">Sie können jetzt im geöffneten übergeordneten **Recordset** -Objekt navigieren und auf die untergeordneten **Recordset** -Detailobjekte zugreifen. Weitere Informationen finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="3edc3-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="3edc3-175">**Übergeordnete und untergeordnete Detailergebnisdatensätze**</span><span class="sxs-lookup"><span data-stu-id="3edc3-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="3edc3-176">**Übergeordnet**</span><span class="sxs-lookup"><span data-stu-id="3edc3-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edc3-177">SUM (rs.Bevölkerung)</span><span class="sxs-lookup"><span data-stu-id="3edc3-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="3edc3-178">rs</span><span class="sxs-lookup"><span data-stu-id="3edc3-178">rs</span></span></p></th>
<th><p><span data-ttu-id="3edc3-179">Bundesland</span><span class="sxs-lookup"><span data-stu-id="3edc3-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="3edc3-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="3edc3-181">Verweis auf untergeordnetes Recordset (Stufe 1)</span><span class="sxs-lookup"><span data-stu-id="3edc3-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="3edc3-182">Bayern</span><span class="sxs-lookup"><span data-stu-id="3edc3-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="3edc3-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="3edc3-184">Verweis auf untergeordnetes Recordset (Stufe 2)</span><span class="sxs-lookup"><span data-stu-id="3edc3-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="3edc3-185">Hessen</span><span class="sxs-lookup"><span data-stu-id="3edc3-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="3edc3-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="3edc3-187">Verweis auf untergeordnetes Recordset (Stufe 3)</span><span class="sxs-lookup"><span data-stu-id="3edc3-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="3edc3-188">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3edc3-189">**Untergeordneter Knoten 1**</span><span class="sxs-lookup"><span data-stu-id="3edc3-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edc3-190">Bundesland</span><span class="sxs-lookup"><span data-stu-id="3edc3-190">State</span></span></p></th>
<th><p><span data-ttu-id="3edc3-191">Ort</span><span class="sxs-lookup"><span data-stu-id="3edc3-191">City</span></span></p></th>
<th><p><span data-ttu-id="3edc3-192">Bevölkerung</span><span class="sxs-lookup"><span data-stu-id="3edc3-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-193">Bayern</span><span class="sxs-lookup"><span data-stu-id="3edc3-193">CA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-194">München</span><span class="sxs-lookup"><span data-stu-id="3edc3-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="3edc3-195">Um 800.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-196">Bayern</span><span class="sxs-lookup"><span data-stu-id="3edc3-196">CA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-197">Nürnberg</span><span class="sxs-lookup"><span data-stu-id="3edc3-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="3edc3-198">600.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3edc3-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="3edc3-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edc3-200">Bundesland</span><span class="sxs-lookup"><span data-stu-id="3edc3-200">State</span></span></p></th>
<th><p><span data-ttu-id="3edc3-201">Ort</span><span class="sxs-lookup"><span data-stu-id="3edc3-201">City</span></span></p></th>
<th><p><span data-ttu-id="3edc3-202">Bevölkerung</span><span class="sxs-lookup"><span data-stu-id="3edc3-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-203">Hessen</span><span class="sxs-lookup"><span data-stu-id="3edc3-203">WA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-204">Frankfurt</span><span class="sxs-lookup"><span data-stu-id="3edc3-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="3edc3-205">700.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-206">Hessen</span><span class="sxs-lookup"><span data-stu-id="3edc3-206">WA</span></span></p></td>
<td><p><span data-ttu-id="3edc3-207">Offenbach</span><span class="sxs-lookup"><span data-stu-id="3edc3-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="3edc3-208">500.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3edc3-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="3edc3-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edc3-210">Bundesland</span><span class="sxs-lookup"><span data-stu-id="3edc3-210">State</span></span></p></th>
<th><p><span data-ttu-id="3edc3-211">Ort</span><span class="sxs-lookup"><span data-stu-id="3edc3-211">City</span></span></p></th>
<th><p><span data-ttu-id="3edc3-212">Bevölkerung</span><span class="sxs-lookup"><span data-stu-id="3edc3-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-213">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-213">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-214">Köln</span><span class="sxs-lookup"><span data-stu-id="3edc3-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="3edc3-215">200.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edc3-216">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-216">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-217">Düsseldorf</span><span class="sxs-lookup"><span data-stu-id="3edc3-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="3edc3-218">400.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edc3-219">Nordrhein-Westfalen</span><span class="sxs-lookup"><span data-stu-id="3edc3-219">OR</span></span></p></td>
<td><p><span data-ttu-id="3edc3-220">Dortmund</span><span class="sxs-lookup"><span data-stu-id="3edc3-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="3edc3-221">300.000</span><span class="sxs-lookup"><span data-stu-id="3edc3-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

