---
title: Behandeln von Fehlern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Fehler [Infopath 2007], Behandlung, FormErrorCollection [InfoPath 2007], InfoPath 2007, Fehlerbehandlung, FormError [InfoPath 2007], Fehlerbehandlung [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet. Das InfoPath-Objektmodell von Microsoft.Office.InfoPath-Namespace unterstützt die Fehlerbehandlung durch Verwendung der FormError-Klasse in Verbindung mit der FormErrorCollection-Klasse bereitgestellt.
ms.openlocfilehash: 3bfad103c31d0b5364d1c75acfbb2f590f7658bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790755"
---
# <a name="handle-errors"></a><span data-ttu-id="d7844-105">Behandeln von Fehlern</span><span class="sxs-lookup"><span data-stu-id="d7844-105">Handle Errors</span></span>

<span data-ttu-id="d7844-106">Beim Erstellen von benutzerdefinierter Anwendungen müssen Entwickler häufig Fehlerbehandlung ausführen, die Programmierung Schreiben von Code zum Prüfen, ob Fehler, die von der Anwendung ausgelöst oder zum Erstellen und benutzerdefinierte Fehlermeldungen auslösen beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="d7844-106">When creating custom applications, developers must often perform error handling that involves writing programming code to check for errors raised by the application or to create and raise custom errors.</span></span> <span data-ttu-id="d7844-107">Das InfoPath-Objektmodell von [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace unterstützt die Fehlerbehandlung durch Verwendung der [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Klasse in Verbindung mit der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d7844-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports error handling through the use of the [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) class in association with the [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) class.</span></span> 
  
<span data-ttu-id="d7844-108">Fehler in InfoPath können aus den folgenden Gründen auftreten:</span><span class="sxs-lookup"><span data-stu-id="d7844-108">In InfoPath, errors can occur for the following reasons:</span></span>
  
- <span data-ttu-id="d7844-109">Wenn Daten, die in ein Formular eingegeben werden, bei der XML-Schemavalidierung Fehler aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7844-109">When data entered into a form fails XML schema validation.</span></span>
    
- <span data-ttu-id="d7844-110">Wenn eine benutzerdefinierte Validierungseinschränkung Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="d7844-110">When a custom validation constraint fails.</span></span>
    
- <span data-ttu-id="d7844-111">Wenn von der [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode der [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Event-Objekts ein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7844-111">When an error is generated by the [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) method of the [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) event object.</span></span> 
    
- <span data-ttu-id="d7844-112">Wenn ein benutzerdefinierter Fehler erstellt wird mithilfe der [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d7844-112">When a user-defined error is created using the [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) method of the [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) class.</span></span> 
    
## <a name="overview-of-the-formerrorcollection-class"></a><span data-ttu-id="d7844-113">Übersicht über die FormErrorCollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="d7844-113">Overview of the FormErrorCollection Class</span></span>

<span data-ttu-id="d7844-114">[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Objekte zu verwalten, die die Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="d7844-114">The [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) class provides the following methods and properties, which form developers can use to manage the [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) objects that the collection contains.</span></span> 
  
|<span data-ttu-id="d7844-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7844-115">**Name**</span></span>|<span data-ttu-id="d7844-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7844-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7844-117">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methode (+ 3 Überladungen)</span><span class="sxs-lookup"><span data-stu-id="d7844-117">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) method (+3 overloads)</span></span>  <br/> |<span data-ttu-id="d7844-118">Erstellt ein **FormError** -Objekt und fügt es der Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7844-118">Creates a **FormError** object and adds it to the collection.</span></span>  <br/> |
|<span data-ttu-id="d7844-119">[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) -Methode (+ 1 Überladung)</span><span class="sxs-lookup"><span data-stu-id="d7844-119">[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) method (+1 overload)</span></span>  <br/> |<span data-ttu-id="d7844-120">Löscht den angegebenen benutzerdefinierten Fehler aus der Auflistung. </span><span class="sxs-lookup"><span data-stu-id="d7844-120">Deletes the specified user-defined error from the collection.</span></span>  <br/> |
|<span data-ttu-id="d7844-121">[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d7844-121">[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) method</span></span>  <br/> |<span data-ttu-id="d7844-122">Löscht alle **FormError** -Objekte, die in der Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d7844-122">Deletes all **FormError** objects contained in the collection.</span></span>  <br/> |
|<span data-ttu-id="d7844-123">[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 Überladung)</span><span class="sxs-lookup"><span data-stu-id="d7844-123">[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+1 overload)</span></span>  <br/> |<span data-ttu-id="d7844-124">Alle **FormError** -Objekte des angegebenen Namens oder Typs zurückgegeben aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d7844-124">Returns all **FormError** objects of the specified name or type from the collection.</span></span>  <br/> |
|<span data-ttu-id="d7844-125">[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-125">[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-126">Ruft die Anzahl der **FormError** -Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d7844-126">Gets a count of the number of **FormError** objects contained in the collection.</span></span>  <br/> |
|<span data-ttu-id="d7844-127">[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-127">[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-128">Ruft einen Verweis auf ein **FormError** -Objekt basierend auf der angegebenen Indexnummer ab.</span><span class="sxs-lookup"><span data-stu-id="d7844-128">Gets a reference to an **FormError** object based on the specified index number.</span></span>  <br/> |
   
## <a name="overview-of-the-formerror-class"></a><span data-ttu-id="d7844-129">Übersicht über die FormError-Klasse</span><span class="sxs-lookup"><span data-stu-id="d7844-129">Overview of the FormError Class</span></span>

<span data-ttu-id="d7844-130">Die [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Klasse stellt die folgenden Eigenschaften, die Formularentwickler Informationen zu dem Fehler ausgelösten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d7844-130">The [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) class provides the following properties, which form developers can use to access information about the error that was raised.</span></span> 
  
|<span data-ttu-id="d7844-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7844-131">**Name**</span></span>|<span data-ttu-id="d7844-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7844-132">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7844-133">[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-133">[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-134">Dient zum Abrufen oder Festlegen der detaillierten Fehlermeldung des **FormError** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d7844-134">Gets or sets the detailed error message of the **FormError** object.</span></span>  <br/> |
|<span data-ttu-id="d7844-135">[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-135">[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-136">Ruft ab oder legt den Fehlercode des **FormError** -Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="d7844-136">Gets or sets the error code of the **FormError** object.</span></span>  <br/> |
|<span data-ttu-id="d7844-137">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-137">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-138">Ruft ein **XPathNavigator** -Objekt, das auf dem **FormError** -Objekt zugeordneten Knoten positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="d7844-138">Gets an **XPathNavigator** object that is positioned at the node associated with the **FormError** object.</span></span>  <br/> |
|<span data-ttu-id="d7844-139">[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-139">[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-140">Dient zum Abrufen oder Festlegen der kurzen Fehlermeldung des **FormError** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d7844-140">Gets or sets the short error message of the **FormError** object.</span></span>  <br/> |
|<span data-ttu-id="d7844-141">[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7844-141">[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) property</span></span>  <br/> |<span data-ttu-id="d7844-142">Ruft den Typ des **FormError** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="d7844-142">Gets the type of the **FormError** object.</span></span>  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a><span data-ttu-id="d7844-143">Verwenden der Klassen "FormErrorCollection" und "FormError"</span><span class="sxs-lookup"><span data-stu-id="d7844-143">Using the FormErrorCollection and FormError Classes</span></span>

<span data-ttu-id="d7844-144">Der Zugriff auf das einem Formular zugeordnete **FormErrorCollection** -Objekt erfolgt über die [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) -Eigenschaft des [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7844-144">The **FormErrorCollection** object associated with a form is accessed through the [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) object.</span></span> <span data-ttu-id="d7844-145">**FormErrorCollection** -Objekt ist mit einem Formular zugrunde liegenden XML-Dokument verknüpft, sodass tritt ein Fehler auf, es und anderen Fehlern zugegriffen und verwaltet werden können innerhalb des aktuellen XML-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="d7844-145">The **FormErrorCollection** object is associated with a form's underlying XML document so that when an error occurs, it and any additional errors can be accessed and managed within the current XML document.</span></span> <span data-ttu-id="d7844-146">Im folgenden Beispiel wird veranschaulicht, wie eine Schleife verwendet werden kann, um den Fehler zu überprüfen, die in einem Formular zugrunde liegenden XML-Dokument enthalten sein könnten.</span><span class="sxs-lookup"><span data-stu-id="d7844-146">The following example demonstrates how a loop can be used to check the errors that may exist in a form's underlying XML document.</span></span> <span data-ttu-id="d7844-147">Wenn Fehler aufgetreten sind, die Funktion durchläuft jede von ihnen und, mithilfe der **Message** -Eigenschaft des **FormError** -Objekts ein Meldungsfeld für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7844-147">If there are errors, the function loops through each of them, and, using the **Message** property of the **FormError** object, displays a message box to the user.</span></span> 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

<span data-ttu-id="d7844-148">Von einem Ereignishandler für das Formular Daten Validierung konnte die vorstehende-Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d7844-148">The preceding function could be called from one of the form's data validation event handlers.</span></span> <span data-ttu-id="d7844-149">Beispielsweise würde, wenn in den Ereignisdetails Ereignishandler für das [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) -Ereignis eines Felds im Formular verwendet wird, der Aufruf der Funktion das XML-Knoten-Argument mit der [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft des Event-Objekts [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) wie folgt übergeben.</span><span class="sxs-lookup"><span data-stu-id="d7844-149">For example, when used in the event handler for the [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) event of a field in the form, the call to the function would pass the XML node argument using the [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property of the [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) event object as follows.</span></span> 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

<span data-ttu-id="d7844-150">Neben der Behandlung von InfoPath generierten Fehler, können Formularentwickler auch benutzerdefinierte Fehler mithilfe der [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methode der [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) -Event-Objekts oder mithilfe der [Hinzufügen generieren ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)-Methode der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d7844-150">In addition to handling errors generated by InfoPath, form developers can also generate custom errors by using the [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) method of the [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) event object, or by using the [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) method of the [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) class.</span></span> <span data-ttu-id="d7844-151">Informationen zur Verwendung der Methods [ReportError (XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) oder [Hinzufügen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) klicken Sie auf die Links für diese Methoden am Anfang dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="d7844-151">For information about using the [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) or [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods, click the links for those methods at the beginning of this topic.</span></span> 
  
## <a name="handling-managed-code-exceptions"></a><span data-ttu-id="d7844-152">Behandlung von Ausnahmen im verwalteten Code</span><span class="sxs-lookup"><span data-stu-id="d7844-152">Handling Managed-Code Exceptions</span></span>

<span data-ttu-id="d7844-153">Sie können die try-catch-Ausnahmebehandlung zum Behandeln von Ausnahmen verwenden, die in Formularvorlagen mit verwaltetem Code ausgelöst wurden. Dies wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7844-153">You can use try-catch exception handling to handle exceptions raised in managed-code form template as shown in the following code example.</span></span>
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

<span data-ttu-id="d7844-p106">Wenn Sie im Formularcode keine try-catch-Ausnahmebehandlung verwenden, zeigt InfoPath beim Debuggen und Anzeigen der Vorschau Informationen zu unbehandelten Ausnahmen im Dialogfeld für InfoPath-Fehler an. Außerdem werden unbehandelte Ausnahmen im Dialogfeld für InfoPath-Fehler zur Laufzeit standardmäßig nicht angezeigt, wenn Sie die Formularvorlage mit verwaltetem Code bereitstellen. Verwenden Sie das folgende Verfahren, um Informationen zu unbehandelten Ausnahmen zur Laufzeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7844-p106">If you do not use try-catch exception handling in your form code, InfoPath will display information about unhandled exceptions in the InfoPath error dialog box while debugging and previewing. Additionally, by default, unhandled exceptions are not displayed in the InfoPath error dialog box at run time when you deploy your managed-code form template. To display information about unhandled exceptions at run time, use the following procedure.</span></span>
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a><span data-ttu-id="d7844-157">Aktivieren von Benachrichtigungen zu unbehandelten Ausnahmen im verwalteten Code zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="d7844-157">Enable notifications for unhandled managed-code exceptions at run time</span></span>

1. <span data-ttu-id="d7844-158">Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf die Registerkarte **Datei** .</span><span class="sxs-lookup"><span data-stu-id="d7844-158">Open the InfoPath designer, and then click the **File** tab.</span></span> 
    
2. <span data-ttu-id="d7844-159">Klicken Sie auf **Optionen**, und klicken Sie dann unter der Kategorie **Allgemein** auf **InfoPath-Optionen** .</span><span class="sxs-lookup"><span data-stu-id="d7844-159">Click **Options**, and then click **InfoPath Options** under the **General** category.</span></span> 
    
3. <span data-ttu-id="d7844-160">Wählen Sie auf der Registerkarte **Erweitert** das Kontrollkästchen **Benachrichtigung für Fehler in Visual Basic und C#-Code anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="d7844-160">On the **Advanced** tab, select the **Show a notification for Visual Basic and C# code errors** check box.</span></span> 
    
