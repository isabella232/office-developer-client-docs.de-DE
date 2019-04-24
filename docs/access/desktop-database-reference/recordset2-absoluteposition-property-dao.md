---
title: Recordset2. AbsolutePosition-Eigenschaft (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4de869866e2aeb28032553be78bee7af16f60402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307511"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="39bb3-102">Recordset2. AbsolutePosition-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="39bb3-102">Recordset2.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="39bb3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39bb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39bb3-104">Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset2**-Objekts fest oder gibt die Nummer zurück.</span><span class="sxs-lookup"><span data-stu-id="39bb3-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39bb3-105">Syntax</span></span>

<span data-ttu-id="39bb3-106">*Ausdruck* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="39bb3-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="39bb3-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="39bb3-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bb3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39bb3-108">Remarks</span></span>

<span data-ttu-id="39bb3-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span><span class="sxs-lookup"><span data-stu-id="39bb3-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="39bb3-p102">Da der Wert der **AbsolutePosition**-Eigenschaft auf Null basiert (d. h. der Wert 0 bezieht sich auf den ersten Datensatz im **Recordset2**-Objekt), kann er nicht auf einen Wert gesetzt werden, der größer oder gleich der Anzahl der enthaltenen Datensätze ist. Falls dies geschieht, wird ein auffangbarer Fehler verursacht. Sie können die Anzahl der gefüllten Datensätze im **Recordset2**-Objekt feststellen, indem Sie den Wert der **RecordCount**-Eigenschaft überprüfen. Der maximale Wert der **AbsolutePosition**-Eigenschaft ist der Wert der **RecordCount**-Eigenschaft minus 1.</span><span class="sxs-lookup"><span data-stu-id="39bb3-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="39bb3-114">Wenn kein aktueller Datensatz vorhanden ist, wie wenn im **Recordset2** -Objekt keine Datensätze vorhanden sind, gibt **AbsolutePosition** -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="39bb3-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="39bb3-115">Wenn der aktuelle Datensatz gelöscht wird, wird der Wert der **AbsolutePosition** -Eigenschaft nicht definiert, und es tritt ein abfangbarer Fehler auf, wenn darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="39bb3-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="39bb3-116">Neue Datensätze werden am Ende der Sequenz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="39bb3-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="39bb3-p104">Sie sollten diese Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Lesezeichen sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Möglichkeit, den aktuellen Datensatz in allen Typen von **Recordset2**-Objekten zu positionieren. Die Position eines Datensatzes ändert sich, wenn ein oder mehr vorangehende Datensätze gelöscht werden. Außerdem gibt es keine Gewähr, dass ein Datensatz die gleiche absolute Position hat, wenn das **Recordset2**-Objekt neu erstellt wird, da die Reihenfolge einzelner Datensätze innerhalb eines **Recordset**-Objekts nicht garantiert ist, außer das Objekt wird mit einer SQL-Anweisung unter Verwendung einer ORDER BY-Klausel erstellt.</span><span class="sxs-lookup"><span data-stu-id="39bb3-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="39bb3-p105">Wenn Sie die **AbsolutePosition**-Eigenschaft für ein soeben geöffnetes und noch nicht aufgefülltes **Recordset2**-Objekt auf einen größeren Wert als Null festlegen, wird ein auffangbarer Fehler verursacht. Füllen Sie das **Recordset2**-Objekt zuerst mit der **MoveLast**-Methode.</span><span class="sxs-lookup"><span data-stu-id="39bb3-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset2** object causes a trappable error. Populate the **Recordset2** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="39bb3-123">Die **AbsolutePosition** -Eigenschaft ist nicht für Forward-Only- **Recordset2** -Objekte oder für **Recordset2** -Objekte verfügbar, die von Passthrough-Abfragen für mit Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="39bb3-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset2** objects, or on **Recordset2** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="39bb3-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="39bb3-124">Example</span></span>

<span data-ttu-id="39bb3-125">In diesem Beispiel wird die Verarbeitung einer Schleife, die alle Datensätze eines **Recordset2**-Objekts durchläuft, mit der **AbsolutePosition**-Eigenschaft verfolgt.</span><span class="sxs-lookup"><span data-stu-id="39bb3-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
