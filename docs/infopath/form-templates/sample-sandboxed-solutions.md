---
title: Beispiel-Sandkastenlösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Dieses Thema enthält zwei Beispiele, in denen die Art von Code angezeigt wird, den Sie in einer Sandbox-Lösung in InfoPath schreiben können, und wie die Formularvorlage veröffentlicht wird.
ms.openlocfilehash: 56a9a2a765100ef327790265c7cf734903268bed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303500"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="758ed-103">Beispiel-Sandkastenlösungen</span><span class="sxs-lookup"><span data-stu-id="758ed-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="758ed-104">InfoPath-Formulare mit verwaltetem Code können im InfoPath-Designer in der SharePoint-Sandbox-Lösungsinfrastruktur veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="758ed-104">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer.</span></span> <span data-ttu-id="758ed-105">Dieses Thema enthält zwei Beispiele, in denen die Art von Code angezeigt wird, den Sie in einer Sandbox-Lösung in InfoPath schreiben können, und wie die Formularvorlage veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="758ed-105">This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="758ed-106">Beispiel 1: Sortieren von Daten in einem Bestellformular</span><span class="sxs-lookup"><span data-stu-id="758ed-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="758ed-107">Eine sinnvolle Aufgabe, die Sie mithilfe von Code in einem InfoPath-Formular ausführen können, besteht darin, Daten in einer wiederholten Tabelle zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="758ed-107">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table.</span></span> <span data-ttu-id="758ed-108">Hierzu werden die Knoten im zugrunde liegenden XML-Dokument, die im InfoPath-Formular angezeigt werden, neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="758ed-108">To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form.</span></span> <span data-ttu-id="758ed-109">Obwohl das in diesem Thema beschriebene Szenario für die Veröffentlichung direkt aus InfoPath als sandkastenlösung vorgesehen ist, kann es auch als vom Administrator genehmigte Formularvorlage bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="758ed-109">Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="758ed-110">Stellen Sie vor Beginn sicher, dass die folgenden Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="758ed-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="758ed-111">Sie sind Websitesammlungsadministrator auf der SharePoint Server 2010-oder SharePoint Foundation 2010-Website, auf der Sie das Formular veröffentlichen möchten.</span><span class="sxs-lookup"><span data-stu-id="758ed-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="758ed-112">Erkundigen Sie sich beim Farmadministrator, ob der Microsoft SharePoint Foundation-Sandkasten-Code Dienst auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="758ed-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="758ed-113">Weitere Informationen finden Sie unter [Veröffentlichen von Formularen mit Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="758ed-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="758ed-114">Sie haben als Programmiersprache für die Formularvorlage **C#** oder **Visual Basic** ohne früheren Versionsnamen dahinter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="758ed-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="758ed-115">Die InfoPath 2007-kompatiblen und InfoPath 2003-kompatiblen Versionen der Programmiersprachen und Objektmodelle werden für sandkastenlösungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="758ed-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="758ed-116">Weitere Informationen dazu, wie Sie die Programmiersprache angeben, finden Sie unter [develop with Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="758ed-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="758ed-117">Führen Sie die folgenden Schritte aus, um eine Formularvorlage zu erstellen, durch die die Daten in einem **Wiederholte Tabelle**-Steuerelement im Formular sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="758ed-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="758ed-118">So erstellen Sie eine Formularvorlage zum programmatischen Sortieren von Daten im Formular</span><span class="sxs-lookup"><span data-stu-id="758ed-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="758ed-119">Erstellen Sie eine neue Formularvorlage im InfoPath-Designer, und fügen Sie dem Formular ein Steuerelement für **wiederholte Tabellen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="758ed-119">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form.</span></span> <span data-ttu-id="758ed-120">Im Beispielcode für dieses Beispiel werden die Zeilen basierend auf der ersten Spalte in der Tabelle sortiert, aber Sie können den Code leicht ändern, um mit einer beliebigen Spalte zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="758ed-120">The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="758ed-121">Fügen Sie dem Formular ein **Schaltfläche**-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="758ed-121">Add a **Button** control to the form.</span></span> <span data-ttu-id="758ed-122">Der Code zum Sortieren der Tabelle wird dem Ereignishandler für das Clicked-Ereignis der \*\*\*\* Schaltfläche hinzugefügt, aber Sie können zu diesem Zweck auch ein anderes Ereignis verwenden.</span><span class="sxs-lookup"><span data-stu-id="758ed-122">The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="758ed-p107">Wählen Sie die Schaltfläche aus, klicken Sie auf die Registerkarte **Eigenschaften**, und klicken Sie dann auf **Benutzerdefinierter Code**. Wenn das Formular noch nicht gespeichert wurde, werden Sie zum Speichern aufgefordert. Anschließend wird der Code-Editor mit dem Cursor im Ereignishandler der Schaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="758ed-p107">Select the button, click the **Properties** tab, and then click **Custom Code**. If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="758ed-p108">Fügen Sie den folgenden Code in den Ereignishandler der Schaltfläche ein. Durch den Code werden die Elemente aus der ersten Spalte in einem Array platziert, das Array wird sortiert, und dann wird die Tabelle basierend auf dem sortierten Array neu angeordnet. Bei diesem Code wird angenommen, dass es sich bei den zu sortierenden Daten um Zeichenfolgedaten handelt.</span><span class="sxs-lookup"><span data-stu-id="758ed-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. <span data-ttu-id="758ed-128">Veröffentlichen Sie das Formular mithilfe der folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="758ed-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="758ed-129">Klicken Sie auf der Registerkarte **veröffentlichen** in der backStaging auf **SharePoint Server** .</span><span class="sxs-lookup"><span data-stu-id="758ed-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="758ed-130">Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="758ed-131">Sie müssen Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als sandkastenlösung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="758ed-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="758ed-132">Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="758ed-133">Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="758ed-134">Geben Sie den Namen und die Beschreibungen für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="758ed-135">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="758ed-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="758ed-136">Beispiel 2: Verwalten von Kreditoren in einer SharePoint-Liste</span><span class="sxs-lookup"><span data-stu-id="758ed-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="758ed-137">Dieses Beispiel umfasst das Programmieren mit dem Microsoft SharePoint Foundation 2010-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="758ed-137">This example involves programming against the Microsoft SharePoint Foundation 2010 object model.</span></span> <span data-ttu-id="758ed-138">Hierzu müssen Sie einen Verweis auf die Microsoft. SharePoint. dll-Assembly erstellen, die mit einer lizenzierten Kopie von SharePoint Server 2010 installiert wird.</span><span class="sxs-lookup"><span data-stu-id="758ed-138">To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="758ed-139">Microsoft. SharePoint. Server. dll wird standardmäßig in C:\Programme\Microsoft Shared\Web Server Extensions\14\ISAPI installiert.</span><span class="sxs-lookup"><span data-stu-id="758ed-139">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default.</span></span> <span data-ttu-id="758ed-140">Diese DLL muss in Projekten enthalten sein, in denen Sie das SharePoint-Objektmodell programmieren.</span><span class="sxs-lookup"><span data-stu-id="758ed-140">This DLL must be included in projects where you program against the SharePoint object model.</span></span> <span data-ttu-id="758ed-141">Wenn Sie einen Verweis auf die Microsoft. SharePoint. dll in einem Visual Studio 2012-Projekt erstellen möchten, öffnen Sie den **Code-Editor**, und klicken Sie dann im Menü **Extras** auf **Verweis hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="758ed-141">To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu.</span></span> <span data-ttu-id="758ed-142">Klicken Sie im Dialogfeld **Verweis hinzufügen** auf die Registerkarte **Durchsuchen** , geben Sie den Speicherort der Datei Microsoft. SharePoint. dll an, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="758ed-142">In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**.</span></span> <span data-ttu-id="758ed-143">Dadurch wird die Microsoft. SharePoint. dll in das Projektverzeichnis kopiert, sodass Sie die SharePoint Foundation 2010-Objektmodellelemente in Ihrer InfoPath-Lösung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="758ed-143">This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="758ed-144">Entwerfen des Formulars und entwickeln des Codes</span><span class="sxs-lookup"><span data-stu-id="758ed-144">Designing the form and developing the code</span></span>

<span data-ttu-id="758ed-145">Anhand von Code in einem InfoPath-Formular können Sie das SharePoint-Objektmodell verwenden, um Elemente in Nachschlagelisten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="758ed-145">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists.</span></span> <span data-ttu-id="758ed-146">Dies ist hilfreich, wenn Sie ein Dropdownfeld aus einer SharePoint-Liste auffüllen und neue Werte hinzufügen möchten, ohne ein separates Formular zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="758ed-146">This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form.</span></span> <span data-ttu-id="758ed-147">In diesem Beispiel wird ein Kombinationsfeld verwendet, um alle Werte anzuzeigen, die derzeit in der Liste enthalten sind, und es wird eine Programmierlogik erstellt, um den Wert zur Liste hinzuzufügen, falls dieser noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="758ed-147">This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="758ed-148">So erstellen Sie eine Formularvorlage zum Hinzufügen neuer Elemente zu einem Kombinationsfeld, das auf einer SharePoint-Liste basiert</span><span class="sxs-lookup"><span data-stu-id="758ed-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="758ed-149">Erstellen Sie eine einfache benutzerdefinierte Liste auf einem SharePoint Server 2010-Server, und nennen Sie Sie myList.</span><span class="sxs-lookup"><span data-stu-id="758ed-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="758ed-150">Im folgenden Beispiel wird ein **Kombinationsfeld** verwendet, das an das Feld **Title** dieser Liste gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="758ed-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="758ed-151">Erstellen Sie ein neues **leeres Formular** in InfoPath Designer, fügen Sie ein **Kombinationsfeld** -Steuerelement in das Formular ein, und benennen Sie das Feld, das an das Kombinationsfeld gebunden ist, in mycombo um.</span><span class="sxs-lookup"><span data-stu-id="758ed-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="758ed-152">Erstellen Sie die Datenverbindung mit der Liste, die zum Auffüllen des Kombinationsfelds verwendet werden soll, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="758ed-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="758ed-153">Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Externe Daten** auf die Schaltfläche**Aus SharePoint-Liste**.</span><span class="sxs-lookup"><span data-stu-id="758ed-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="758ed-154">Geben Sie die URL der Website ein, die die Liste enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="758ed-155">Wählen Sie die Liste aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="758ed-156">Wählen Sie die einzuschließenden Felder aus (in diesem Beispiel Title und ID).</span><span class="sxs-lookup"><span data-stu-id="758ed-156">Select the fields that you want to include, for this example, select Title and ID.</span></span> <span data-ttu-id="758ed-157">Title enthält die Werte zum Nachschlagen.</span><span class="sxs-lookup"><span data-stu-id="758ed-157">Title contains the values for lookup.</span></span> <span data-ttu-id="758ed-158">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-158">Click **Next**.</span></span>
        
    5. <span data-ttu-id="758ed-159">Klicken Sie auf dem folgenden Bildschirm auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="758ed-160">Benennen Sie die Datenverbindung Lookuplist, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="758ed-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="758ed-161">Füllen Sie die Werte im Kombinationsfeld aus der Liste aus, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="758ed-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="758ed-162">Wählen Sie das in Schritt 1 erstellte Kombinationsfeld aus.</span><span class="sxs-lookup"><span data-stu-id="758ed-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="758ed-163">Klicken Sie auf der Registerkarte **Eigenschaften von Steuerelementtools** des Menübands auf **Auswahlmöglichkeiten bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="758ed-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="758ed-164">Wählen Sie **Auswahl aus einer externen Datenquelle abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="758ed-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="758ed-165">Stellen Sie sicher, dass **Datenquelle** auf die in Schritt 2 erstellte Datenverbindung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="758ed-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="758ed-166">Legen Sie den Wert und den Anzeigenamen auf Title fest.</span><span class="sxs-lookup"><span data-stu-id="758ed-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="758ed-167">Wählen Sie auf der Registerkarte **Browser Formulare** **immer** unter **Postfacheinstellungen**aus, und klicken Sie dann auf **OK** , um das DialogfeldEigenschaften zu schließen.</span><span class="sxs-lookup"><span data-stu-id="758ed-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="758ed-168">Stellen Sie sicher, dass das Kombinationsfeld weiterhin ausgewählt ist, und klicken Sie dann auf der Registerkarte **Entwicklertools** des Menübands auf **geändert** .</span><span class="sxs-lookup"><span data-stu-id="758ed-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="758ed-169">Wenn das Formular noch nicht gespeichert wurde, werden Sie zum Speichern aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="758ed-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="758ed-170">Und dann wird das Code-Editor-Fenster mit dem Cursor im `myCombo_Changed` Ereignishandler geöffnet.</span><span class="sxs-lookup"><span data-stu-id="758ed-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="758ed-171">Fügen Sie wie weiter oben in diesem Thema beschrieben einen Verweis auf die Microsoft.SharePoint.dll-Assembly hinzu.</span><span class="sxs-lookup"><span data-stu-id="758ed-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="758ed-172">Weitere Informationen zum Verweisen auf die Microsoft. SharePoint-Assembly finden Sie unter [use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="758ed-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="758ed-173">Fügen Sie den folgenden Code in `myCombo_Changed` den Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="758ed-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. <span data-ttu-id="758ed-174">Das obige Codebeispiel hängt von der `GetDomValue` Hilfsfunktion ab.</span><span class="sxs-lookup"><span data-stu-id="758ed-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="758ed-175">Fügen Sie den folgenden Code für `GetDomValue` die Hilfsfunktion unter `myCombo_Changed` der Ereignishandlerfunktion ein.</span><span class="sxs-lookup"><span data-stu-id="758ed-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. <span data-ttu-id="758ed-176">Veröffentlichen Sie das Formular mithilfe der folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="758ed-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="758ed-177">Klicken Sie auf der Registerkarte **veröffentlichen** in der backStaging auf **SharePoint Server** .</span><span class="sxs-lookup"><span data-stu-id="758ed-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="758ed-178">Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="758ed-179">Sie müssen Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als sandkastenlösung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="758ed-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="758ed-180">Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="758ed-181">Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="758ed-182">Geben Sie den Namen und die Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="758ed-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="758ed-183">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="758ed-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="758ed-184">Nachdem das Formular erfolgreich veröffentlicht wurde, öffnen Sie das Formular aus der Formularbibliothek, und fügen Sie im Kombinationsfeld einen neuen Wert hinzu, um den Code zu testen.</span><span class="sxs-lookup"><span data-stu-id="758ed-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="758ed-185">Wenn Sie das myCombo-Feld beenden, wird der neue Wert in die SharePoint-Liste geschrieben.</span><span class="sxs-lookup"><span data-stu-id="758ed-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

