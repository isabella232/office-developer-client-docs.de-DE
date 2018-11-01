---
title: Errors Collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: debc3554fb63ab379bbc94bc8d44e2239eb32dd4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885752"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="7bdf5-102">Errors Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bdf5-102">Errors Collection (DAO)</span></span>


<span data-ttu-id="7bdf5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bdf5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bdf5-104">Eine **Errors**-Auflistung enthält alle gespeicherten **Error**-Objekte, die sich jeweils auf eine einzelne DAO-Operation beziehen.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bdf5-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bdf5-105">Remarks</span></span>

<span data-ttu-id="7bdf5-p101">Jede Operation, die DAO-Objekte betrifft, kann Fehler generieren. Wenn ein Fehler auftritt, werden eines oder mehrere der **Error**-Objekte in der **Errors**-Auflistung des **DBEngine**-Objekts abgelegt. Wenn eine andere DAO-Operation einen Fehler generiert, wird die **Errors**-Auflistung gelöscht, und der neue Satz von **Error**-Objekten wird in der **Errors**-Auflistung abgelegt. Das Objekt mit der höchsten Zahl in der **Errors**-Auflistung (DBEngine.Errors.Count - 1) entspricht dem Fehler, der vom VBA-Objekt (Microsoft Visual Basic für Applikationen) **Err** gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-p101">Any operation involving DAO objects can generate one or more errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object. When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection. The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="7bdf5-110">DAO-Operationen, die keinen Fehler verursachen, haben keine Auswirkung auf die **Errors**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="7bdf5-111">Im Gegensatz zu anderen Auflistungen werden an die **Errors**-Auflistung keine Elemente angefügt. Die **Errors**-Auflistung unterstützt daher nicht die Methoden **Append** und **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="7bdf5-p102">Der Satz von **Error**-Objekten in der **Errors**-Auflistung beschreibt jeweils einen Fehler. Das erste **Error**-Objekt bezieht sich auf den Fehler unterster Ebene, das zweite Objekt auf die nächsthöhere Ebene usw. Wenn beispielsweise beim Versuch, ein **[Recordset](recordset-object-dao.md)** -Objekt zu öffnen, ein ODBC-Fehler auftritt, enthält das erste Fehlerobjekt den ODBC-Fehler der untersten Ebene. Nachfolgende Fehler enthalten die ODBC-Fehler, die von den verschiedenen ODBC-Ebenen zurückgegeben werden. In diesem Fall werden vom ODBC-Treibermanager und möglicherweise vom Treiber selbst separate **Error**-Objekte zurückgegeben. Das letzte **Error**-Objekt enthält den DAO-Fehler, der angibt, dass das Objekt nicht geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-p102">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error, the second the next higher level, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="7bdf5-117">Dadurch, dass die genauen Fehler in der **Errors**-Auflistung aufgeführt werden, können die Fehlerbehandlungsroutinen die Fehlerursache genauer bestimmen und entsprechende Wiederherstellungsschritte einleiten.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <span data-ttu-id="7bdf5-p103">[!HINWEIS] Wenn Sie das Objekt, das entweder vor oder während des Einfügens in die **Errors**-Auflistung einen Fehler verursacht, mit dem Schlüsselwort **New** erstellt haben, enthält die Auflistung keine Fehlerinformationen zu diesem Objekt, da das neue Objekt nicht dem **DBEngine**-Objekt zugeordnet ist. Die Fehlerinformationen sind jedoch im VBA-Objekt **Err** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-p103">If you use the **New** keyword to create an object that causes an error either before or while being placed into the **Errors** collection, the collection doesn't contain error information about that object, because the new object is not associated with the **DBEngine** object. However, the error information is available in the VBA **Err** object.</span></span>

## <a name="example"></a><span data-ttu-id="7bdf5-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7bdf5-120">Example</span></span>

<span data-ttu-id="7bdf5-121">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="7bdf5-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

