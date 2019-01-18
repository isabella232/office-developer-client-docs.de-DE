---
title: Recordset.AbsolutePosition-Eigenschaft (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702504"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="16881-102">Recordset.AbsolutePosition-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="16881-102">Recordset.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="16881-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16881-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16881-104">Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset** -Objekts fest oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="16881-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="16881-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16881-105">Syntax</span></span>

<span data-ttu-id="16881-106">*Ausdruck* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="16881-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="16881-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="16881-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16881-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16881-108">Remarks</span></span>

<span data-ttu-id="16881-p101">Sie können die **AbsolutePosition** -Eigenschaft verwenden, um den aktuellen Datensatzzeiger basierend auf seiner Position in einem **Recordset** -Objekt vom Typ Dynaset oder Momentaufnahme auf einen bestimmten Datensatz zu verschieben. Sie können auch die aktuelle Datensatznummer ermitteln, indem Sie die Einstellung der **AbsolutePosition** -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="16881-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="16881-p102">Da es sich bei der **AbsolutePosition** -Eigenschaft um einen nullbasierten Wert handelt (d. h. die Einstellung 0 verweist auf den ersten Datensatz im **Recordset** -Objekt), können Sie keinen Wert festlegen, der größer oder gleich der Anzahl von im enthaltenen Datensätzen ist. Falls Sie das versuchen, tritt ein abfangbarer Fehler auf. Ermitteln Sie die Anzahl von im **Recordset** -Objekt enthaltenen Datensätzen, indem Sie die Einstellung der **RecordCount** -Eigenschaft überprüfen. Die maximal zulässige Einstellung für die **AbsolutePosition** -Eigenschaft entspricht dem Wert der **RecordCount** -Eigenschaft minus 1.</span><span class="sxs-lookup"><span data-stu-id="16881-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="16881-114">Wenn kein aktueller Datensatz vorhanden ist, als wenn keine Datensätze im **Recordset** -Objekt vorhanden sind, gibt **AbsolutePosition** -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="16881-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="16881-115">Wenn der aktuelle Datensatz gelöscht wird, der Wert der **AbsolutePosition** -Eigenschaft ist nicht definiert, und wenn auf sie verwiesen wird, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="16881-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="16881-116">Neue Datensätze werden am Ende der Sequenz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="16881-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="16881-p104">Verwenden Sie diese Eigenschaft nicht als Ersatz-Datensatznummer. Textmarken sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von **Recordset** -Objekten. Die Position eines Datensatzes ändert sich insbesondere dann, wenn einer oder mehrere vorausgehende Datensätze gelöscht werden. Außerdem kann nicht davon ausgegangen werden, dass ein bestimmter Datensatz beim erneuten Erstellen des **Recordset** -Objekts die gleiche absolute Position aufweist. Denn die Reihenfolge einzelner Datensätze in einem **Recordset** -Objekt ist nur dann sichergestellt, wenn es in einer SQL-Anweisung mit einer ORDER BY-Klausel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="16881-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="16881-p105">Wird die **AbsolutePosition**-Eigenschaft bei einem neu geöffneten, jedoch leeren **Recordset**-Objekt auf einen Wert größer als Null festgelegt, tritt ein abfangbarer Fehler auf. Füllen Sie das **Recordset**-Objekt zuerst mit der **MoveLast**-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="16881-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error. Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="16881-123">Die **AbsolutePosition**-Eigenschaft ist bei **Recordset**-Objekten des Typs Vorwärts nicht verfügbar. Sie ist auch bei **Recordset**-Objekten nicht verfügbar, die von Pass-Through-Abfragen zu ODBC-Datenbanken, die mit dem Microsoft Access-Datenbankmodul verbunden sind, geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="16881-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="16881-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="16881-124">Example</span></span>

<span data-ttu-id="16881-125">Dieses Beispiel verwendet die **AbsolutePosition** -Eigenschaft, um den Status einer Schleife nachzuverfolgen, in der alle Datensätze eines **Recordset** -Objekts aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="16881-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
