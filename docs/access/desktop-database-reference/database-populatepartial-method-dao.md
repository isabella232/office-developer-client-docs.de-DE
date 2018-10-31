---
title: Database.PopulatePartial Method (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fa52050e91c1a291dd59f9cde1ea36c320406dd6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860266"
---
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="44705-102">Database.PopulatePartial Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="44705-102">Database.PopulatePartial Method (DAO)</span></span>


<span data-ttu-id="44705-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44705-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="44705-p101">Synchronisiert alle Änderungen in einem Teilreplikat mit dem vollständigen Repliktat, löscht alle Datensätze im Teilreplikat, und füllt dann das Teilreplikat auf Basis der aktuellen Replikatfilter erneut auf (gilt nur für Microsoft Access-Datenbanken).</span><span class="sxs-lookup"><span data-stu-id="44705-p101">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="44705-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="44705-106">Syntax</span></span>

<span data-ttu-id="44705-107">*Ausdruck* . PopulatePartial (***DbPathName***)</span><span class="sxs-lookup"><span data-stu-id="44705-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="44705-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="44705-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="44705-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="44705-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44705-110">Name</span><span class="sxs-lookup"><span data-stu-id="44705-110">Name</span></span></p></th>
<th><p><span data-ttu-id="44705-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="44705-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="44705-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="44705-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="44705-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44705-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44705-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="44705-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="44705-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="44705-115">Required</span></span></p></td>
<td><p><span data-ttu-id="44705-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="44705-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="44705-117">Der Pfad und Name des vollständigen Replikats, aus dem Datensätze aufgefüllt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44705-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="44705-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44705-118">Remarks</span></span>

<span data-ttu-id="44705-119">Wenn Sie ein Teilreplikat mit einem vollständigen Replikat synchronisieren, ist es möglich, "verwaiste" Datensätze aus dem Teilreplikat zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44705-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="44705-120">Angenommen, Sie haben eine Kundentabelle mit seiner **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** legen Sie auf "Region = 'CA'".</span><span class="sxs-lookup"><span data-stu-id="44705-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="44705-121">Wenn ein Benutzer die Region eines Kunden von CA in NY in dem Teilreplikat ändert, und dann eine über die **[Synchronize](database-synchronize-method-dao.md)** -Methode Synchronisation, die Änderung an das vollständige Replikat weitergegeben, aber der Datensatz mit NY im Teilreplikat ist verwaist, da nun It nicht erfüllen die Replikatfilterkriterien.</span><span class="sxs-lookup"><span data-stu-id="44705-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="44705-p103">Mit der **PopulatePartial**-Methode lässt sich das Problem der verwaisten Datensätze vermeiden. Die **PopulatePartial**-Methode ähnelt der **Synchronize**-Methode, synchronisiert allerdings alle Änderungen mit dem vollständigen Repliktat, entfernt alle Datensätze im Teilreplikat, und füllt anschließend das Teilreplikat auf Basis der aktuellen Replikatfilter erneut auf. Auch wenn sich die Replikatfilter nicht geändert haben, werden mit **PopulatePartial** immer sämtliche Datensätze im Teilreplikat entfernt, und dann wird es auf Basis der aktuellen Filter neu aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="44705-p103">To solve the problem of orphaned records, you can use the **PopulatePartial** method. The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters. Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="44705-p104">Die **PopulatePartial**-Methode sollten Sie immer dann verwenden, wenn Sie ein Teilreplikat erstellen und wenn Sie die Replikatfilter ändern. Werden Replikatfilter durch die Anwendung geändert, sollten Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="44705-p104">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters. If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="44705-127">Synchronisieren Sie das vollständige Repliktat mit dem Teilreplikat, in dem die Filter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="44705-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="44705-128">Verwenden Sie die Eigenschaften **ReplicaFilter** und **[PartialReplica](relation-partialreplica-property-dao.md)**, um die gewünschten Änderungen an den Replikatfiltern vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="44705-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="44705-129">Rufen Sie die **PopulatePartial**-Methode auf, um alle Datensätze aus dem Teilreplikat zu entfernen und alle Datensätze aus dem vollständigen Repliktat zu übertragen, die den neuen Replikatfilterkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="44705-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="44705-130">Wenn ein Replikatfilter geändert wurde und die **Synchronize**-Methode ohne vorherigen Aufruf von **PopulatePartial** aufgerufen wird, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="44705-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="44705-p105">Die **PopulatePartial**-Methode kann nur für ein Teilreplikat aufgerufen werden, das exklusiv geöffnet ist. Darüber hinaus kann die **PopulatePartial**-Methode nicht über Code aufgerufen werden, der innerhalb des Teilreplikats ausgeführt wird. Öffnen Sie das Teilreplikat stattdessen exklusiv aus dem vollständigen Repliktat oder einer anderen Datenbank, und rufen Sie dann **PopulatePartial** auf.</span><span class="sxs-lookup"><span data-stu-id="44705-p105">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access. Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself. Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <span data-ttu-id="44705-p106">[!HINWEIS] Obwohl **PopulatePartial** vor dem Löschen und erneuten Auffüllen des Teilreplikats eine einseitige Synchronisierung durchführt, ist es empfehlenswert, **Synchronize** vor **PopulatePartial** aufzurufen. Wenn das Aufrufen von **Synchronize** fehlschlägt, tritt ein abfangbarer Fehler auf. Anhand dieses Fehlers können Sie entscheiden, ob Sie mit der **PopulatePartial**-Methode fortfahren möchten (bei der alle Datensätze im Teilreplikat entfernt werden). Wird **PopulatePartial** selbst aufgerufen und tritt während der Synchronisierung der Datensätze ein Fehler auf, werden die Datensätze im Teilreplikat auf jeden Fall gelöscht, auch wenn dies nicht Ihre Absicht war.</span><span class="sxs-lookup"><span data-stu-id="44705-p106">Although **PopulatePartial** performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call **Synchronize** before calling **PopulatePartial**. This is because if the call to **Synchronize** fails, a trappable error occurs. You can use this error to decide whether or not to proceed with the **PopulatePartial** method (which removes all records in the partial replica). If **PopulatePartial** is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span>



## <a name="example"></a><span data-ttu-id="44705-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44705-138">Example</span></span>

<span data-ttu-id="44705-139">Im folgenden Beispiel wird die **PopulatePartial**-Methode nach dem Ändern eines Replikatfilters verwendet.</span><span class="sxs-lookup"><span data-stu-id="44705-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

