---
title: Error-Objekt - Datenzugriff Objekte (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4a42fdf47b736b13cea53122431606224d2f9da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889560"
---
# <a name="error-object-dao"></a><span data-ttu-id="dd697-102">Error Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd697-102">Error Object (DAO)</span></span>


<span data-ttu-id="dd697-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd697-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd697-104">Das **Error**-Objekt enthält Details zu Datenzugriffsfehlern. Dabei bezieht sich jeder Fehler auf eine einzelne Operation, an der DAO beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="dd697-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd697-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd697-105">Remarks</span></span>

<span data-ttu-id="dd697-p101">Jede Operation, an der DAO beteiligt ist, kann mindestens einen Fehler generieren. Beispielsweise kann ein Aufruf an einen ODBC-Server zu einem Fehler des Datenbankservers, einem Fehler von ODBC und einem DAO-Fehler führen. Sobald einer dieser Fehler auftritt, wird ein **Error**-Objekt in die **Errors**-Auflistung des **DBEngine**-Objekts aufgenommen. Ein einzelnes Ereignis kann somit mehrere **Error**-Objekte ergeben, die in der **Errors**-Auflistung anzeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd697-p101">Any operation involving DAO can generate one or more errors. For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error. As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object. A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="dd697-p102">Generiert eine anschließende DAO-Operation einen Fehler, wird die **Errors**-Auflistung gelöscht, und die neuen **Error**-Objekte werden in die **Errors**-Auflistung aufgenommen. DAO-Operationen, die keinen Fehler generieren, wirken sich nicht auf die **Errors**-Auflistung aus.</span><span class="sxs-lookup"><span data-stu-id="dd697-p102">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection. DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="dd697-p103">Die Gruppe der **Error**-Objekte in der **Errors**-Auflistung beschreibt einen Fehler. Das erste **Error**-Objekt ist der Fehler der niedrigsten Ebene (der verursachende Fehler), das zweite Objekt ist der Fehler der nächsten Ebene usw. Tritt z. B. ein ODBC-Fehler beim Öffnen eines **[Recordset](recordset-object-dao.md)** -Objekts auf, enthält das erste **Error**-Objekt, **Errors**(0), den ODBC-Fehler der niedrigsten Ebene; die folgenden Fehler enthalten ODBC-Fehler, die von den verschiedenen ODBC-Schichten zurückgegeben werden. In diesem Fall geben der ODBC-Treibermanager und möglicherweise direkt der Treiber gesonderte **Error**-Objekte zurück. Das letzte **Error**-Objekt, **Errors.Count-** 1, enthält den DAO-Fehler mit dem Hinweis, dass das Objekt nicht geöffnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="dd697-p103">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="dd697-p104">Das Auflisten der speziellen Fehler in der **Errors**-Auflistung ermöglicht den Fehlerbehandlungsroutinen eine präzisere Ermittlung der Fehlerursache und das Durchführen der richtigen Schritte zur Wiederherstellung. Sie können die Eigenschaften des **Error**-Objekts lesen, um die folgenden Details zu den einzelnen Fehlern zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="dd697-p104">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover. You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="dd697-119">Die **[Description](error-description-property-dao.md)** -Eigenschaft mit dem Text der Fehlermeldung, die beim Abfangen des Fehlers auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dd697-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="dd697-120">Die **[Anzahl](error-number-property-dao.md)** -Eigenschaft, die den Long Integer-Wert der Fehlerkonstante enthält.</span><span class="sxs-lookup"><span data-stu-id="dd697-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="dd697-p105">Die **[Source](error-source-property-dao.md)** -Eigenschaft, die das Objekt identifiziert, das den Fehler verursacht hat. Das ist besonders nützlich, wenn sich nach einem Aufruf der ODBC-Datenquelle mehrere **Error**-Objekte in der **Errors**-Auflistung befinden.</span><span class="sxs-lookup"><span data-stu-id="dd697-p105">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="dd697-123">Die Eigenschaften **HelpFile** und **HelpContext**, die jeweils die betreffende Microsoft Windows-Hilfedatei und das Hilfethema (sofern vorhanden) zu dem Fehler angeben.</span><span class="sxs-lookup"><span data-stu-id="dd697-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="dd697-124">Wenn in Microsoft Visual Basic für Applikationen (VBA) programmieren, wenn Sie das **New** -Schlüsselwort verwenden, um ein Objekt zu erstellen, die anschließend, tritt ein Fehler vor hat dieses Objekt einer Auflistung, das **DBEngine** -Objekt **Fehler** angefügt wurden Auflistung enthalten keinen Eintrag für dieses Objekt Fehler; sein, da das neue Objekt nicht das **DBEngine** -Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd697-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the **New** keyword to create an object that subsequently causes an error before that object has been appended to a collection, the **DBEngine** object's **Errors** collection won't contain an entry for that object's error, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="dd697-125">Die Fehlerinformationen sind jedoch im VBA-Objekt **Err** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd697-125">However, the error information is available in the VBA **Err** object.</span></span> <span data-ttu-id="dd697-126">Der VBA-Code für die Fehlerbehandlung sollten die **Errors** -Auflistung untersuchen, wenn Sie einen Fehler beim Datenzugriff erwarten.</span><span class="sxs-lookup"><span data-stu-id="dd697-126">Your VBA error-handling code should examine the **Errors** collection whenever you anticipate a data access error.</span></span> <span data-ttu-id="dd697-127">Wenn Sie einen zentralen Fehlerhandler schreiben, testen Sie die VBA **Err** -Objekts, um festzustellen, ob die Fehlerinformationen in der **Errors** -Auflistung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="dd697-127">If you are writing a centralized error handler, test the VBA **Err** object to determine if the error information in the **Errors** collection is valid.</span></span> <span data-ttu-id="dd697-128">Wenn die **Number** -Eigenschaft des letzten Elements der **Errors** -Auflistung (DBEngine.Errors.Count - 1) und der Wert der Übereinstimmung **Err** -Objekt, anschließend können Sie eine Reihe von **Select Case** -Anweisung zum Identifizieren des bestimmten DAO-Fehlers oder aufgetretenen Fehler.</span><span class="sxs-lookup"><span data-stu-id="dd697-128">If the **Number** property of the last element of the **Errors** collection (DBEngine.Errors.Count - 1) and the value of the **Err** object match, you can then use a series of **Select Case** statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="dd697-129">Wenn sie nicht übereinstimmen, verwenden Sie die [Refresh](errors-refresh-method-dao.md) -Methode auf die **Errors** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="dd697-129">If they do not match, use the [Refresh](errors-refresh-method-dao.md) method on the **Errors** collection.</span></span>



## <a name="example"></a><span data-ttu-id="dd697-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dd697-130">Example</span></span>

<span data-ttu-id="dd697-131">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="dd697-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

