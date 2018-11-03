---
title: TableDef.ReplicaFilter-Eigenschaft (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dbd8ecc670742d6b9f88dd9c608d2304e26a8d09
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929664"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="4a962-102">TableDef.ReplicaFilter-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a962-102">TableDef.ReplicaFilter property (DAO)</span></span>


<span data-ttu-id="4a962-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a962-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a962-p101">Legt einen Wert für ein **[TableDef](tabledef-object-dao.md)** -Objekt in einem Teilreplikat fest, der angibt, welche Teilmenge von Datensätzen in der Tabelle aus einem vollständigen Replikat repliziert werden soll, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="4a962-p101">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a962-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a962-106">Syntax</span></span>

<span data-ttu-id="4a962-107">*Ausdruck* . ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="4a962-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="4a962-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a962-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a962-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a962-109">Remarks</span></span>

<span data-ttu-id="4a962-110">Die Einstellung bzw. der Rückgabewert ist ein **String**- oder **Boolean**-Datentyp, der angibt, welche Teilmenge von Datensätzen repliziert wird, wie in der folgenden Tabelle aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="4a962-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a962-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4a962-111">Value</span></span></p></th>
<th><p><span data-ttu-id="4a962-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a962-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a962-113">Eine Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4a962-113">A string</span></span></p></td>
<td><p><span data-ttu-id="4a962-114">Ein Kriterium,  das die Teilreplikattabelle erfüllen muss, damit sie vom vollständigen Replikat repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4a962-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a962-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="4a962-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="4a962-116">Alle Datensätze werden repliziert.</span><span class="sxs-lookup"><span data-stu-id="4a962-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a962-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="4a962-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="4a962-118">(Standardwert) Kein Datensatz wird repliziert.</span><span class="sxs-lookup"><span data-stu-id="4a962-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a962-119">Diese Eigenschaft ist ähnlich einer SQL WHERE-Klausel (ohne das Wort WHERE). Es ist jedoch nicht möglich, Unterabfragen, Aggregatfunktionen (wie etwa **Count**) oder benutzerdefinierte Funktionen innerhalb der Kriterien festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4a962-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="4a962-p102">Sie können nur Daten zwischen einem vollständigen und einem Teilkreplikat replizieren. Es ist nicht möglich, Daten zwischen zwei Teilreplikaten zu synchronisieren. Sie können auch Einschränkungen für Teilreplikate hinsichtlich der zu replizierenden Datensätze festlegen, aber nicht angeben, welche Felder repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a962-p102">You can only synchronize data between a full replica and a partial replica. You can't synchronize data between two partial replicas. Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="4a962-p103">Gewöhnlich legen Sie einen Replikatfilter fest, wenn Sie eine andere Gruppe von Datensätzen replizieren wollen. Wenn z. B. ein Vertriebsmitarbeiter vorübergehend die Vertriebsregion eines anderen Mitarbeiters übernimmt, kann die Datenbankanwendung vorübergehend Daten für beide Regionen replizieren und dann zum vorherigen Filter zurückkehren. In diesem Szenario setzt die Anwendung die **ReplicaFilter**-Eigenschaft zurück und füllt dann das Teilreplikat auf.</span><span class="sxs-lookup"><span data-stu-id="4a962-p103">Usually, you reset a replica filter when you want to replicate a different set of records. For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter. In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="4a962-126">Wenn Ihre Anwendung Replikatfilter ändert, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="4a962-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="4a962-127">Replizieren Sie das vollständige Replikat mit dem Teilreplikat, in dem die Filter geändert werden, mithilfe der **[Synchronize](database-synchronize-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="4a962-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="4a962-128">Nehmen Sie mithilfe der **ReplicaFilter**-Eigenschaft die gewünschten Änderungen am Replikatfilter vor.</span><span class="sxs-lookup"><span data-stu-id="4a962-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="4a962-129">Entfernen Sie alle Datensätze aus dem Teilreplikat, und übertragen Sie mithilfe der **[PopulatePartial](database-populatepartial-method-dao.md)** -Methode alle Datensätze aus dem vollständigen Replikat, die die neuen Replikatfilterkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4a962-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="4a962-p104">Sie können einen Filter entfernen, indem Sie für die **ReplicaFilter**-Eigenschaft den Wert **False** festlegen. Wenn Sie alle Filter entfernen und die **PopulatePartial**-Methode aufrufen, erscheinen keine Datensätze in den replizierten Tabellen im Teilreplikat.</span><span class="sxs-lookup"><span data-stu-id="4a962-p104">To remove a filter, set the **ReplicaFilter** property to **False**. If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4a962-132">[!HINWEIS] Wenn ein Replikatfilter geändert wurde und die <STRONG>Synchronize</STRONG>-Methode aufgerufen wird, ohne zuvor <STRONG>PopulatePartial</STRONG> aufzurufen, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4a962-132">If a replica filter has changed, and the <STRONG>Synchronize</STRONG> method is invoked without first invoking <STRONG>PopulatePartial</STRONG>, a trappable error occurs.</span></span></P>



## <a name="example"></a><span data-ttu-id="4a962-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a962-133">Example</span></span>

<span data-ttu-id="4a962-134">In dem folgenden Beispiel wird die ReplicaFilter-Eigenschaft verwendet, um nur Kundendatensätze aus der Region Kalifornien (CA) zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="4a962-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

