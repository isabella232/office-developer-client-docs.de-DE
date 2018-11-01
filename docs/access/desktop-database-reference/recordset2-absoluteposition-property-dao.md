---
title: Recordset2.AbsolutePosition Property (DAO)
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
ms.openlocfilehash: c5eb8c80743b5fac17f7a3c8d11080863e511eb8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888601"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="d3066-102">Recordset2.AbsolutePosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3066-102">Recordset2.AbsolutePosition Property (DAO)</span></span>


<span data-ttu-id="d3066-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3066-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3066-104">Legt die relative Datensatznummer des aktuellen Datensatzes eines **Recordset2**-Objekts fest oder gibt die Nummer zurück.</span><span class="sxs-lookup"><span data-stu-id="d3066-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3066-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3066-105">Syntax</span></span>

<span data-ttu-id="d3066-106">*Ausdruck* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="d3066-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="d3066-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3066-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3066-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3066-108">Remarks</span></span>

<span data-ttu-id="d3066-p101">Mit der AbsolutePosition-Eigenschaft können Sie den aktuellen Datensatzzeiger basierend auf seiner Ordnungsposition in einem Recordset2-Objekt vom Typ Dynaset oder Momentaufnahme auf einen bestimmten Datensatz festlegen. Sie können die aktuelle Datensatznummer auch feststellen, indem Sie die AbsolutePosition-Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d3066-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="d3066-p102">Da der Wert der **AbsolutePosition**-Eigenschaft auf Null basiert (d. h. der Wert 0 bezieht sich auf den ersten Datensatz im **Recordset2**-Objekt), kann er nicht auf einen Wert gesetzt werden, der größer oder gleich der Anzahl der enthaltenen Datensätze ist. Falls dies geschieht, wird ein auffangbarer Fehler verursacht. Sie können die Anzahl der gefüllten Datensätze im **Recordset2**-Objekt feststellen, indem Sie den Wert der **RecordCount**-Eigenschaft überprüfen. Der maximale Wert der **AbsolutePosition**-Eigenschaft ist der Wert der **RecordCount**-Eigenschaft minus 1.</span><span class="sxs-lookup"><span data-stu-id="d3066-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="d3066-114">Wenn kein aktueller Datensatz vorhanden ist, als wenn im **Recordset2** -Objekt keine Datensätze vorhanden sind, gibt **AbsolutePosition** -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="d3066-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="d3066-115">Wenn der aktuelle Datensatz gelöscht wird, der Wert der **AbsolutePosition** -Eigenschaft ist nicht definiert, und wenn auf sie verwiesen wird, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d3066-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="d3066-116">Neue Datensätze werden am Ende der Sequenz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d3066-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="d3066-p104">Sie sollten diese Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Lesezeichen sind weiterhin die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Möglichkeit, den aktuellen Datensatz in allen Typen von **Recordset2**-Objekten zu positionieren. Die Position eines Datensatzes ändert sich, wenn ein oder mehr vorangehende Datensätze gelöscht werden. Außerdem gibt es keine Gewähr, dass ein Datensatz die gleiche absolute Position hat, wenn das **Recordset2**-Objekt neu erstellt wird, da die Reihenfolge einzelner Datensätze innerhalb eines **Recordset**-Objekts nicht garantiert ist, außer das Objekt wird mit einer SQL-Anweisung unter Verwendung einer ORDER BY-Klausel erstellt.</span><span class="sxs-lookup"><span data-stu-id="d3066-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="d3066-p105">Wenn Sie die <STRONG>AbsolutePosition</STRONG>-Eigenschaft für ein soeben geöffnetes und noch nicht aufgefülltes <STRONG>Recordset2</STRONG>-Objekt auf einen größeren Wert als Null festlegen, wird ein auffangbarer Fehler verursacht. Füllen Sie das <STRONG>Recordset2</STRONG>-Objekt zuerst mit der <STRONG>MoveLast</STRONG>-Methode.</span><span class="sxs-lookup"><span data-stu-id="d3066-p105">Setting the <STRONG>AbsolutePosition</STRONG> property to a value greater than zero on a newly opened but unpopulated <STRONG>Recordset2</STRONG> object causes a trappable error. Populate the <STRONG>Recordset2</STRONG> object first with the <STRONG>MoveLast</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="d3066-123">Die <STRONG>AbsolutePosition</STRONG> -Eigenschaft ist nicht verfügbar, auf Forward Typ <STRONG>Recordset2</STRONG> -Objekte oder auf <STRONG>Recordset2</STRONG> -Objekte, die von Pass-Through-Abfragen für Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d3066-123">The <STRONG>AbsolutePosition</STRONG> property isn't available on forward–only–type <STRONG>Recordset2</STRONG> objects, or on <STRONG>Recordset2</STRONG> objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="d3066-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3066-124">Example</span></span>

<span data-ttu-id="d3066-125">In diesem Beispiel wird die Verarbeitung einer Schleife, die alle Datensätze eines **Recordset2**-Objekts durchläuft, mit der **AbsolutePosition**-Eigenschaft verfolgt.</span><span class="sxs-lookup"><span data-stu-id="d3066-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

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
