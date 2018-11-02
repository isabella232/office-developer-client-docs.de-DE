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
# <a name="tabledefreplicafilter-property-dao"></a>TableDef.ReplicaFilter-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert für ein **[TableDef](tabledef-object-dao.md)** -Objekt in einem Teilreplikat fest, der angibt, welche Teilmenge von Datensätzen in der Tabelle aus einem vollständigen Replikat repliziert werden soll, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . ReplicaFilter

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein **String**- oder **Boolean**-Datentyp, der angibt, welche Teilmenge von Datensätzen repliziert wird, wie in der folgenden Tabelle aufgeführt:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Eine Zeichenfolge</p></td>
<td><p>Ein Kriterium,  das die Teilreplikattabelle erfüllen muss, damit sie vom vollständigen Replikat repliziert wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Alle Datensätze werden repliziert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(Standardwert) Kein Datensatz wird repliziert.</p></td>
</tr>
</tbody>
</table>


Diese Eigenschaft ist ähnlich einer SQL WHERE-Klausel (ohne das Wort WHERE). Es ist jedoch nicht möglich, Unterabfragen, Aggregatfunktionen (wie etwa **Count**) oder benutzerdefinierte Funktionen innerhalb der Kriterien festzulegen.

Sie können nur Daten zwischen einem vollständigen und einem Teilkreplikat replizieren. Es ist nicht möglich, Daten zwischen zwei Teilreplikaten zu synchronisieren. Sie können auch Einschränkungen für Teilreplikate hinsichtlich der zu replizierenden Datensätze festlegen, aber nicht angeben, welche Felder repliziert werden sollen.

Gewöhnlich legen Sie einen Replikatfilter fest, wenn Sie eine andere Gruppe von Datensätzen replizieren wollen. Wenn z. B. ein Vertriebsmitarbeiter vorübergehend die Vertriebsregion eines anderen Mitarbeiters übernimmt, kann die Datenbankanwendung vorübergehend Daten für beide Regionen replizieren und dann zum vorherigen Filter zurückkehren. In diesem Szenario setzt die Anwendung die **ReplicaFilter**-Eigenschaft zurück und füllt dann das Teilreplikat auf.

Wenn Ihre Anwendung Replikatfilter ändert, sollten Sie die folgenden Schritte ausführen:

1.  Replizieren Sie das vollständige Replikat mit dem Teilreplikat, in dem die Filter geändert werden, mithilfe der **[Synchronize](database-synchronize-method-dao.md)** -Methode.

2.  Nehmen Sie mithilfe der **ReplicaFilter**-Eigenschaft die gewünschten Änderungen am Replikatfilter vor.

3.  Entfernen Sie alle Datensätze aus dem Teilreplikat, und übertragen Sie mithilfe der **[PopulatePartial](database-populatepartial-method-dao.md)** -Methode alle Datensätze aus dem vollständigen Replikat, die die neuen Replikatfilterkriterien erfüllen.

Sie können einen Filter entfernen, indem Sie für die **ReplicaFilter**-Eigenschaft den Wert **False** festlegen. Wenn Sie alle Filter entfernen und die **PopulatePartial**-Methode aufrufen, erscheinen keine Datensätze in den replizierten Tabellen im Teilreplikat.


> [!NOTE]
> <P>[!HINWEIS] Wenn ein Replikatfilter geändert wurde und die <STRONG>Synchronize</STRONG>-Methode aufgerufen wird, ohne zuvor <STRONG>PopulatePartial</STRONG> aufzurufen, tritt ein auffangbarer Fehler auf.</P>



## <a name="example"></a>Beispiel

In dem folgenden Beispiel wird die ReplicaFilter-Eigenschaft verwendet, um nur Kundendatensätze aus der Region Kalifornien (CA) zu replizieren.

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

