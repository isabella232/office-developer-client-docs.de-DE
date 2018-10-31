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
# <a name="databasepopulatepartial-method-dao"></a>Database.PopulatePartial Method (DAO)


**Betrifft**: Access 2013 | Office 2013


Synchronisiert alle Änderungen in einem Teilreplikat mit dem vollständigen Repliktat, löscht alle Datensätze im Teilreplikat, und füllt dann das Teilreplikat auf Basis der aktuellen Replikatfilter erneut auf (gilt nur für Microsoft Access-Datenbanken).

## <a name="syntax"></a>Syntax

*Ausdruck* . PopulatePartial (***DbPathName***)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

### <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DbPathName</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Pfad und Name des vollständigen Replikats, aus dem Datensätze aufgefüllt werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Teilreplikat mit einem vollständigen Replikat synchronisieren, ist es möglich, "verwaiste" Datensätze aus dem Teilreplikat zu erstellen. Angenommen, Sie haben eine Kundentabelle mit seiner **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** legen Sie auf "Region = 'CA'". Wenn ein Benutzer die Region eines Kunden von CA in NY in dem Teilreplikat ändert, und dann eine über die **[Synchronize](database-synchronize-method-dao.md)** -Methode Synchronisation, die Änderung an das vollständige Replikat weitergegeben, aber der Datensatz mit NY im Teilreplikat ist verwaist, da nun It nicht erfüllen die Replikatfilterkriterien.

Mit der **PopulatePartial**-Methode lässt sich das Problem der verwaisten Datensätze vermeiden. Die **PopulatePartial**-Methode ähnelt der **Synchronize**-Methode, synchronisiert allerdings alle Änderungen mit dem vollständigen Repliktat, entfernt alle Datensätze im Teilreplikat, und füllt anschließend das Teilreplikat auf Basis der aktuellen Replikatfilter erneut auf. Auch wenn sich die Replikatfilter nicht geändert haben, werden mit **PopulatePartial** immer sämtliche Datensätze im Teilreplikat entfernt, und dann wird es auf Basis der aktuellen Filter neu aufgefüllt.

Die **PopulatePartial**-Methode sollten Sie immer dann verwenden, wenn Sie ein Teilreplikat erstellen und wenn Sie die Replikatfilter ändern. Werden Replikatfilter durch die Anwendung geändert, sollten Sie wie folgt vorgehen:

1.  Synchronisieren Sie das vollständige Repliktat mit dem Teilreplikat, in dem die Filter geändert werden.

2.  Verwenden Sie die Eigenschaften **ReplicaFilter** und **[PartialReplica](relation-partialreplica-property-dao.md)**, um die gewünschten Änderungen an den Replikatfiltern vorzunehmen.

3.  Rufen Sie die **PopulatePartial**-Methode auf, um alle Datensätze aus dem Teilreplikat zu entfernen und alle Datensätze aus dem vollständigen Repliktat zu übertragen, die den neuen Replikatfilterkriterien entsprechen.

Wenn ein Replikatfilter geändert wurde und die **Synchronize**-Methode ohne vorherigen Aufruf von **PopulatePartial** aufgerufen wird, tritt ein abfangbarer Fehler auf.

Die **PopulatePartial**-Methode kann nur für ein Teilreplikat aufgerufen werden, das exklusiv geöffnet ist. Darüber hinaus kann die **PopulatePartial**-Methode nicht über Code aufgerufen werden, der innerhalb des Teilreplikats ausgeführt wird. Öffnen Sie das Teilreplikat stattdessen exklusiv aus dem vollständigen Repliktat oder einer anderen Datenbank, und rufen Sie dann **PopulatePartial** auf.


> [!NOTE]
> [!HINWEIS] Obwohl **PopulatePartial** vor dem Löschen und erneuten Auffüllen des Teilreplikats eine einseitige Synchronisierung durchführt, ist es empfehlenswert, **Synchronize** vor **PopulatePartial** aufzurufen. Wenn das Aufrufen von **Synchronize** fehlschlägt, tritt ein abfangbarer Fehler auf. Anhand dieses Fehlers können Sie entscheiden, ob Sie mit der **PopulatePartial**-Methode fortfahren möchten (bei der alle Datensätze im Teilreplikat entfernt werden). Wird **PopulatePartial** selbst aufgerufen und tritt während der Synchronisierung der Datensätze ein Fehler auf, werden die Datensätze im Teilreplikat auf jeden Fall gelöscht, auch wenn dies nicht Ihre Absicht war.



## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die **PopulatePartial**-Methode nach dem Ändern eines Replikatfilters verwendet.

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

