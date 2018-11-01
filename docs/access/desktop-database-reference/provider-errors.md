---
title: Anbieterfehler (Access PC-Datenbank-Referenz)
TOCTitle: Provider Errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 18d226ff8ff270705d8e30425f83eabc289383b1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883246"
---
# <a name="provider-errors"></a><span data-ttu-id="1cc52-102">Anbieterfehler</span><span class="sxs-lookup"><span data-stu-id="1cc52-102">Provider Errors</span></span>


<span data-ttu-id="1cc52-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cc52-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="1cc52-p101">Wenn ein Anbieterfehler auftritt, wird der Laufzeitfehler -2147467259 zurückgegeben. Wenn dieser Fehler angezeigt wird, überprüfen Sie die **Errors** -Auflistung des aktiven **Connection** -Objekts, die mindestens einen Fehler mit einer Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p101">When a provider error occurs, a run-time error of -2147467259 is returned. When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="1cc52-106">Errors-Auflistung von ADO</span><span class="sxs-lookup"><span data-stu-id="1cc52-106">The ADO Errors Collection</span></span>

<span data-ttu-id="1cc52-p102">Ein ADO-Vorgang kann mehrere Anbieterfehler generieren. Deshalb macht ADO mithilfe des **Connection** -Objekts eine Auflistung mit Fehlerobjekten verfügbar. Diese Auflistung enthält keine Objekte, wenn ein Vorgang erfolgreich abgeschlossen wird. Sie enthält mindestens ein **Error** -Objekt, wenn etwas schief gelaufen ist und der Anbieter mindestens einen Fehler ausgelöst hat. Überprüfen Sie die einzelnen Fehlerobjekte, um die genaue Ursache des Fehlers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p102">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object. This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors. Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="1cc52-p103">Wenn Sie alle aufgetretenen Fehler behandelt haben, können Sie die Auflistung durch Aufrufen der **Clear** -Methode leeren. Es ist sehr wichtig, dass die **Errors** -Auflistung geleert wird, bevor Sie die Methoden **Resync**, **UpdateBatch** oder **CancelBatch** für ein **Recordset** -Objekt aufrufen, die **Open** -Methode für ein **Connection** -Objekt aufrufen, oder die **Filter** -Eigenschaft für ein **Recordset** -Objekt festlegen. Durch das explizite Leeren der Auflistung haben Sie die Sicherheit, dass in der Auflistung keine **Error** -Objekte von einem vorherigen Vorgang mehr übrig sind.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p103">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method. It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object. By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="1cc52-p104">Bei manchen Vorgängen können Warnungen sowie Fehler generiert werden. Warnungen werden ebenfalls durch **Error** -Objekte in der **Errors** -Auflistung dargestellt. Wenn ein Anbieter der Auflistung eine Warnung hinzufügt, wird kein Laufzeitfehler generiert. Überprüfen Sie die **Count** -Eigenschaft der **Errors** -Auflistung, um festzustellen, ob von einem bestimmten Vorgang eine Warnung erzeugt wurde. Falls ein Wert von mindestens eins vorhanden ist, wurde der Auflistung ein **Error** -Objekt hinzugefügt. Wenn Sie festgestellt haben, dass die **Errors** -Auflistung Fehler oder Warnungen enthält, können Sie die Auflistung durchlaufen und Informationen zu jedem vorhandenen **Error** -Objekt abrufen. Dies wird anhand des folgenden kurzen Visual Basic-Beispiels veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="1cc52-p104">Some operations can generate warnings as well as errors. Warnings are also represented by **Error** objects in the **Errors** collection. When a provider adds a warning to the collection, it does not generate a run-time error. Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation. If the count is one or greater, an **Error** object has been added to the collection. Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains. The following short Visual Basic example demonstrates this:</span></span>

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

<span data-ttu-id="1cc52-p105">Die Fehlerbehandlungsroutine enthält eine **For Each** -Schleife, mit der jedes Objekt in der **Errors** -Auflistung überprüft wird. In diesem Beispiel wird lediglich eine Meldung zur Anzeige erfasst. Bei einem funktionierenden Programm würden Sie Code erstellen, um für jeden Fehler eine entsprechende Aufgabe auszuführen, wie z. B. alle geöffneten Dateien schließen und das Programm auf geordnete Weise herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p105">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection. In this example, it simply accumulates a message for display. In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="1cc52-123">Error-Objekt</span><span class="sxs-lookup"><span data-stu-id="1cc52-123">The Error Object</span></span>

<span data-ttu-id="1cc52-p106">Durch das Überprüfen eines **Error** -Objekts können Sie bestimmen, welcher Fehler aufgetreten ist und, was noch wichtiger ist, welche Anwendung oder welches Objekt den Fehler verursachte. Das **Error** -Objekt weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="1cc52-p106">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error. The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cc52-126">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1cc52-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="1cc52-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cc52-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cc52-128"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-129">Beschreibender Text für den aufgetretenen Fehler.</span><span class="sxs-lookup"><span data-stu-id="1cc52-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cc52-130"><strong>HelpContext-und HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-131">Das Hilfethema und die Hilfedatei, die eine Beschreibung des aufgetretenen Fehlers enthalten.</span><span class="sxs-lookup"><span data-stu-id="1cc52-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cc52-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-133">Die anbieterspezifische Fehlernummer.</span><span class="sxs-lookup"><span data-stu-id="1cc52-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cc52-134"><strong>Number</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-135">Eine Zahl vom Datentyp Long Integer für die Nummer (aufgeführt in ErrorValueEnum) des aufgetretenen Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1cc52-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cc52-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-137">Gibt den Namen des Objekts oder der Anwendung an, das bzw. die einen Fehler generierte.</span><span class="sxs-lookup"><span data-stu-id="1cc52-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cc52-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="1cc52-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="1cc52-139">Ein aus fünf Zeichen bestehender Fehlercode, den der Anbieter während der Verarbeitung einer SQL-Anweisung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cc52-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cc52-p107">Das **Error** -Objekt von ADO ist weitgehend identisch mit dem standardmäßigen **Err** -Objekt von Visual Basic. Dessen Eigenschaften beschreiben den aufgetretenen Fehler. Neben der Fehlernummer erhalten Sie auch zwei zusammengehörige Informationselemente. Die **NativeError** -Eigenschaft enthält eine Fehlernummer speziell für den verwendeten Anbieter. Im vorherigen Beispiel wird der Microsoft OLE DB-Anbieter für SQL Server verwendet, weshalb **NativeError** Fehler speziell für SQL Server enthält. Die **SQLState** -Eigenschaft weist einen aus fünf Zeichen bestehenden Code auf, mit dem ein Fehler in einer SQL-Anweisung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p107">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object. Its properties describe the error that occurred. In addition to the number of the error, you also receive two related pieces of information. The **NativeError** property contains an error number specific to the provider you are using. In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server. The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="1cc52-146">Ereignisbezogene Fehler</span><span class="sxs-lookup"><span data-stu-id="1cc52-146">Event-Related Errors</span></span>

<span data-ttu-id="1cc52-p108">Das **Error** -Objekt wird auch verwendet, wenn ereignisbezogene Fehler auftreten. Sie können bestimmen, ob im Prozess ein Fehler aufgetreten ist, durch den ein ADO-Ereignis ausgelöst wurde, indem Sie das **Error** -Objekt überprüfen, das als Ereignisparameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p108">The **Error** object is also used when event-related errors occur. You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="1cc52-p109">Wenn der Vorgang, der ein Ereignis verursachte, erfolgreich abgeschlossen wird, wird der *adStatus*-Parameter des Ereignishandlers auf *adStatusOK* festgelegt. Wenn andernfalls der Vorgang, der das Ereignis auslöste, nicht erfolgreich war, wird der *adStatus*-Parameter auf *adStatusErrorsOccurred* festgelegt. In diesem Fall enthält der *pError*-Parameter ein **Error**-Objekt, das den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1cc52-p109">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*. On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*. In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

