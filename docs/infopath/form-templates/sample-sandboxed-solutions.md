---
title: Beispiele für sandkastenlösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Dieses Thema enthält zwei Beispiele, in denen der Art der Code zeigt an, dass Sie in einer InfoPath-sandkastenlösung und zum Veröffentlichen der Formularvorlage schreiben können.
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790837"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="f35cd-103">Beispiele für sandkastenlösungen</span><span class="sxs-lookup"><span data-stu-id="f35cd-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="f35cd-104">InfoPath-Formulare mit verwaltetem Code können aus dem InfoPath-Designer mit der SharePoint-Infrastruktur sandkastenlösung veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-104">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer.</span></span> <span data-ttu-id="f35cd-105">Dieses Thema enthält zwei Beispiele, in denen der Art der Code zeigt an, dass Sie in einer InfoPath-sandkastenlösung und zum Veröffentlichen der Formularvorlage schreiben können.</span><span class="sxs-lookup"><span data-stu-id="f35cd-105">This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="f35cd-106">In Beispiel 1: Sortieren von Daten in einem Bestellformular</span><span class="sxs-lookup"><span data-stu-id="f35cd-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="f35cd-107">Eine nützliche Aufgabe, die Sie ausführen können, mithilfe von Code in einem InfoPath-Formular ist zum Sortieren von Daten in einer wiederholten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f35cd-107">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table.</span></span> <span data-ttu-id="f35cd-108">Zu diesem Zweck ordnet der Code die Knoten in der zugrunde liegenden XML-Dokument, das im InfoPath-Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f35cd-108">To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form.</span></span> <span data-ttu-id="f35cd-109">Obwohl das in diesem Thema beschriebene Szenario für die Veröffentlichung direkt in InfoPath als sandkastenlösung gerichtet ist, können sie auch als vom Administrator genehmigten Formularvorlage bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-109">Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="f35cd-110">Stellen Sie vor Beginn sicher, dass die folgenden Anforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f35cd-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="f35cd-111">Sie sind Administrator einer Websitesammlung auf der SharePoint Server 2010 oder SharePoint Foundation 2010-Website, in dem Sie das Formular veröffentlichen möchten.</span><span class="sxs-lookup"><span data-stu-id="f35cd-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="f35cd-112">Überprüfen Sie mit dem Farmadministrator, um sicherzustellen, dass der Microsoft SharePoint Foundation Sandboxed Code-Dienst auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f35cd-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="f35cd-113">Weitere Informationen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="f35cd-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="f35cd-114">Die Programmiersprache, die Sie für die Formularvorlage ausgewählt haben ist entweder **c#** oder **Visual Basic** nach dem ohne einen beliebigen Versionsnamen der früheren.</span><span class="sxs-lookup"><span data-stu-id="f35cd-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="f35cd-115">Die InfoPath 2007-kompatiblen und InfoPath 2003-kompatiblen Versionen der Programmiersprachen und Objektmodelle werden für sandkastenlösungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f35cd-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="f35cd-116">Weitere Informationen zum Angeben der Programmiersprache finden Sie unter [Entwickeln mit Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="f35cd-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="f35cd-117">Führen Sie die folgenden Schritte aus, um eine Formularvorlage zu erstellen, die die Daten in einem **Wiederholte Tabelle** -Steuerelement im Formular sortiert.</span><span class="sxs-lookup"><span data-stu-id="f35cd-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="f35cd-118">So erstellen Sie eine Formularvorlage zum programmatischen Sortieren von Daten im Formular</span><span class="sxs-lookup"><span data-stu-id="f35cd-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="f35cd-119">Erstellen Sie eine neue Formularvorlage im InfoPath-Designer, und fügen Sie ein Steuerelement **Wiederholte Tabelle** auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="f35cd-119">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form.</span></span> <span data-ttu-id="f35cd-120">Der Beispielcode in diesem Beispiel werden die Zeilen basierend auf der ersten Spalte in der Tabelle sortiert, aber Sie können den Code zum Arbeiten mit einer beliebigen Spalte ganz einfach ändern.</span><span class="sxs-lookup"><span data-stu-id="f35cd-120">The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="f35cd-121">Fügen Sie dem Formular ein **Button** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f35cd-121">Add a **Button** control to the form.</span></span> <span data-ttu-id="f35cd-122">Der Code zum Sortieren der Tabelle wird der Ereignishandler für die Schaltfläche **Clicked** -Ereignis hinzugefügt werden, aber Sie können auch ein anderes Ereignis für diesen Zweck verwenden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-122">The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="f35cd-123">Wählen Sie die Schaltfläche aus, klicken Sie auf der Registerkarte **Eigenschaften** , und klicken Sie dann auf **Benutzerdefinierter Code**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-123">Select the button, click the **Properties** tab, and then click **Custom Code**.</span></span> <span data-ttu-id="f35cd-124">Wenn das Formular noch nicht gespeichert wurde, Sie werden aufgefordert, ihn zu speichern, und klicken Sie dann im Code-Editor wird mit dem Mauszeiger in-Ereignishandler der Schaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f35cd-124">If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="f35cd-p108">Fügen Sie den folgenden Code in den Ereignishandler der Schaltfläche ein. Durch den Code werden die Elemente aus der ersten Spalte in einem Array platziert, das Array wird sortiert, und dann wird die Tabelle basierend auf dem sortierten Array neu angeordnet. Bei diesem Code wird angenommen, dass es sich bei den zu sortierenden Daten um Zeichenfolgedaten handelt.</span><span class="sxs-lookup"><span data-stu-id="f35cd-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
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

5. <span data-ttu-id="f35cd-128">Veröffentlichen Sie das Formular mithilfe der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f35cd-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="f35cd-129">Klicken Sie auf der Registerkarte **Veröffentlichen** in der Backstage-Ansicht auf **SharePoint Server** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="f35cd-130">Geben Sie die URL der SharePoint-Website veröffentlichen, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="f35cd-131">Sie müssen ein Websitesammlungsadministrator auf dieser Website zum Veröffentlichen dieser Formularvorlage als sandkastenlösung sein.</span><span class="sxs-lookup"><span data-stu-id="f35cd-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="f35cd-132">Wählen Sie **Formularbibliothek**aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="f35cd-133">Wählen Sie **eine neue Formularbibliothek erstellen**aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="f35cd-134">Geben Sie den Namen und eine Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="f35cd-135">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="f35cd-136">Beispiel 2: Verwalten von Anbietern in einer SharePoint-Liste</span><span class="sxs-lookup"><span data-stu-id="f35cd-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="f35cd-137">In diesem Beispiel umfasst Programmieren mit dem Microsoft SharePoint Foundation 2010-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="f35cd-137">This example involves programming against the Microsoft SharePoint Foundation 2010 object model.</span></span> <span data-ttu-id="f35cd-138">Zu diesem Zweck müssen Sie einen Verweis auf die Microsoft.SharePoint.dll-Assembly einrichten, die mit eine lizenzierte Version von SharePoint Server 2010 installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f35cd-138">To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="f35cd-139">Microsoft.SharePoint.Server.dll wird in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI standardmäßig installiert.</span><span class="sxs-lookup"><span data-stu-id="f35cd-139">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default.</span></span> <span data-ttu-id="f35cd-140">Diese DLL muss in Projekten, in dem Programmieren der SharePoint-Objektmodell, enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f35cd-140">This DLL must be included in projects where you program against the SharePoint object model.</span></span> <span data-ttu-id="f35cd-141">Wenn Sie einen Verweis auf die Microsoft.SharePoint.dll in einem Projekt auf Visual Studio 2012 eingerichtet haben, öffnen Sie den **Code-Editor**, und klicken Sie dann im Menü **Extras** auf **Verweis hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-141">To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu.</span></span> <span data-ttu-id="f35cd-142">Klicken Sie im Dialogfeld **Verweis hinzufügen** klicken Sie auf die Registerkarte **Durchsuchen** , geben Sie den Speicherort der Microsoft.SharePoint.dll-Datei, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-142">In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**.</span></span> <span data-ttu-id="f35cd-143">Dadurch wird die Microsoft.SharePoint.dll in das Projektverzeichnis kopiert, damit Sie SharePoint Foundation 2010 Objektmodellelemente in InfoPath-Lösung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f35cd-143">This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="f35cd-144">Das Formular entwerfen und Entwickeln des Codes</span><span class="sxs-lookup"><span data-stu-id="f35cd-144">Designing the form and developing the code</span></span>

<span data-ttu-id="f35cd-145">Über Code in einem InfoPath-Formular können Sie das SharePoint-Objektmodell verwenden, Erstellen von Elementen in Nachschlagelisten.</span><span class="sxs-lookup"><span data-stu-id="f35cd-145">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists.</span></span> <span data-ttu-id="f35cd-146">Dies ist nützlich, wenn Sie ein Dropdown-Listenfeld aus einer SharePoint-Liste füllen und neue Werte es hinzufügen, ohne zu ein gesonderten Formular erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f35cd-146">This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form.</span></span> <span data-ttu-id="f35cd-147">In diesem Beispiel wird ein Kombinationsfeld verwendet, um alle der Werte, die derzeit in der Liste angezeigt und erstellt die Programmierlogik der Wert der Liste hinzu, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f35cd-147">This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="f35cd-148">So erstellen Sie eine Formularvorlage zum Hinzufügen neuer Elemente zu einem Kombinationsfeld, das auf einer SharePoint-Liste basiert</span><span class="sxs-lookup"><span data-stu-id="f35cd-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="f35cd-149">Erstellen Sie eine einfache benutzerdefinierte Liste auf einer SharePoint Server 2010-Server, und nennen Sie es MyList.</span><span class="sxs-lookup"><span data-stu-id="f35cd-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="f35cd-150">Im folgenden Beispiel wird ein **Kombinationsfeld** an das Feld **Titel** dieser Liste gebunden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="f35cd-151">Erstellen Sie ein neues **Leeres Formular** im InfoPath-Designer, fügen Sie ein **Kombinationsfeld** -Steuerelement auf Ihrem Formular ein, und benennen Sie das Feld, an das Kombinationsfeld, um in MyCombo gebunden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="f35cd-152">Herstellen der Verbindungs zu der Liste, die zum Auffüllen des Kombinationsfelds mit den folgenden Schritten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f35cd-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="f35cd-153">Klicken Sie auf der Registerkarte **Daten** auf Schaltfläche in der Gruppe **Externe Daten** **Aus SharePoint-Liste** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="f35cd-154">Geben Sie die URL für die Website, die die Liste enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="f35cd-155">Wählen Sie aus der Liste, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="f35cd-156">Wählen Sie die Felder, die Sie aufnehmen möchten, für die in diesem Beispiel wird, wählen Sie Titel und die gleiche ID.</span><span class="sxs-lookup"><span data-stu-id="f35cd-156">Select the fields that you want to include, for this example, select Title and ID.</span></span> <span data-ttu-id="f35cd-157">Titel enthält die Werte für die Suche.</span><span class="sxs-lookup"><span data-stu-id="f35cd-157">Title contains the values for lookup.</span></span> <span data-ttu-id="f35cd-158">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-158">Click **Next**.</span></span>
        
    5. <span data-ttu-id="f35cd-159">Klicken Sie auf dem folgenden Bildschirm auf **Weiter** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="f35cd-160">Nennen Sie die Datenverbindung LookupList, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="f35cd-161">Füllen Sie die Werte im Kombinationsfeld aus der Liste mit den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="f35cd-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="f35cd-162">Wählen Sie das in Schritt 1 erstellte Kombinationsfeld aus.</span><span class="sxs-lookup"><span data-stu-id="f35cd-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="f35cd-163">Klicken Sie auf der Registerkarte **Eigenschaften von Tools** des Menübands auf **Auswahlmöglichkeiten bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="f35cd-164">Wählen Sie **Auswahl aus einer externen Datenquelle abrufen**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="f35cd-165">Stellen Sie sicher, dass **Datenquelle** auf die Datenverbindung festgelegt ist, die Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f35cd-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="f35cd-166">Legen Sie den Wert und den Anzeigenamen auf Title fest.</span><span class="sxs-lookup"><span data-stu-id="f35cd-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="f35cd-167">Klicken Sie auf der Registerkarte **browserformularen** **immer** unter **Postback Einstellungen**wählen Sie aus, und klicken Sie dann auf **OK** , um das Dialogfeld Eigenschaften zu schließen.</span><span class="sxs-lookup"><span data-stu-id="f35cd-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="f35cd-168">Stellen Sie sicher, dass im Kombinationsfeld noch ausgewählt ist, und klicken Sie dann auf der Registerkarte **Entwicklertools** des Menübands auf **Ausgelöstes Ereignis** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="f35cd-169">Wenn das Formular noch nicht gespeichert ist, werden Sie aufgefordert, zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f35cd-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="f35cd-170">Und klicken Sie dann Code-Editor-Fenster wird geöffnet, mit dem Mauszeiger in der `myCombo_Changed` -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="f35cd-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="f35cd-171">Fügen Sie wie weiter oben in diesem Thema beschrieben einen Verweis auf die Microsoft.SharePoint.dll-Assembly hinzu.</span><span class="sxs-lookup"><span data-stu-id="f35cd-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="f35cd-172">Weitere Informationen zum Verweisen auf die Microsoft.SharePoint-Assembly finden Sie unter [SharePoint-Objektmodellmember verwenden](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="f35cd-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="f35cd-173">Fügen Sie den folgenden Code in die `myCombo_Changed` -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="f35cd-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
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

8. <span data-ttu-id="f35cd-174">Im vorherigen Codebeispiel hängt von der `GetDomValue` Hilfsfunktion.</span><span class="sxs-lookup"><span data-stu-id="f35cd-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="f35cd-175">Fügen Sie den folgenden Code für die `GetDomValue` Hilfsfunktion unten die `myCombo_Changed` -Ereignishandlerfunktion.</span><span class="sxs-lookup"><span data-stu-id="f35cd-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
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

9. <span data-ttu-id="f35cd-176">Veröffentlichen Sie das Formular mithilfe der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f35cd-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="f35cd-177">Klicken Sie auf der Registerkarte **Veröffentlichen** in der Backstage-Ansicht auf **SharePoint Server** .</span><span class="sxs-lookup"><span data-stu-id="f35cd-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="f35cd-178">Geben Sie die URL der SharePoint-Website veröffentlichen, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="f35cd-179">Sie müssen ein Websitesammlungsadministrator auf dieser Website zum Veröffentlichen dieser Formularvorlage als sandkastenlösung sein.</span><span class="sxs-lookup"><span data-stu-id="f35cd-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="f35cd-180">Wählen Sie **Formularbibliothek**aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="f35cd-181">Wählen Sie **eine neue Formularbibliothek erstellen**aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="f35cd-182">Geben Sie den Namen und eine Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="f35cd-183">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="f35cd-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="f35cd-184">Nachdem das Formular erfolgreich veröffentlicht wurde, öffnen Sie das Formular in der Formularbibliothek, und fügen Sie einen neuen Wert in das Kombinationsfeld zum Testen des Codes.</span><span class="sxs-lookup"><span data-stu-id="f35cd-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="f35cd-185">Wenn Sie das Feld in MyCombo beenden, wird der neue Wert in der SharePoint-Liste geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f35cd-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

