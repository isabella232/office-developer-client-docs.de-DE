---
title: Beispiel-Sandkastenlösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Dieses Thema enthält zwei Beispiele, die die Art von Code, den Sie in einer InfoPath-Sandkastenlösung schreiben können, und das Veröffentlichen der Formularvorlage veranschaulichen.
ms.openlocfilehash: 9bce60d1141b82343ab021b120ae804d404d6b13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557421"
---
# <a name="sample-sandboxed-solutions"></a>Beispiel-Sandkastenlösungen

InfoPath-Formulare mit verwaltetem Code können über InfoPath Designer in der SharePoint Sandkastenlösungsinfrastruktur veröffentlicht werden. Dieses Thema enthält zwei Beispiele, die die Art von Code, den Sie in einer InfoPath-Sandkastenlösung schreiben können, und das Veröffentlichen der Formularvorlage veranschaulichen.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>Beispiel 1: Sortieren von Daten in einem Bestellformular

Eine hilfreiche Aufgabe, die Sie mithilfe von Code in einem InfoPath-Formular ausführen können, ist das Sortieren von Daten in einer wiederholten Tabelle. Hierzu ordnet der Code die Knoten im zugrunde liegenden XML-Dokument neu an, das im InfoPath-Formular angezeigt wird. Obwohl das in diesem Thema beschriebene Szenario für die direkte Veröffentlichung über InfoPath als Sandkastenlösung vorgesehen ist, kann es auch als vom Administrator genehmigte Formularvorlage bereitgestellt werden.
  
Stellen Sie vor Beginn sicher, dass die folgenden Anforderungen erfüllt sind.
  
- Sie sind Websitesammlungsadministrator auf der Website SharePoint Server 2010 oder SharePoint Foundation 2010, auf der Sie das Formular veröffentlichen möchten.
    
- Wenden Sie sich an den Farmadministrator, um sicherzustellen, dass der Microsoft SharePoint Foundation Sandboxed Code Service auf dem Server ausgeführt wird. Weitere Informationen finden Sie unter [Veröffentlichen von Formularen mit Code.](publishing-forms-with-code.md)
    
- Sie haben als Programmiersprache für die Formularvorlage **C#** oder **Visual Basic** ohne früheren Versionsnamen dahinter ausgewählt. Die Mit InfoPath 2007 und InfoPath 2003 kompatiblen Versionen der Programmiersprachen und Objektmodelle werden für Sandkastenlösungen nicht unterstützt. Weitere Informationen zum Angeben der Programmiersprache finden Sie unter [Entwickeln mit Visual Studio](how-to-develop-with-visual-studio.md).
    
Führen Sie die folgenden Schritte aus, um eine Formularvorlage zu erstellen, durch die die Daten in einem **Wiederholte Tabelle**-Steuerelement im Formular sortiert werden. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>So erstellen Sie eine Formularvorlage zum programmatischen Sortieren von Daten im Formular

1. Erstellen Sie eine neue Formularvorlage im InfoPath-Designer, und fügen Sie dem Formular ein Steuerelement Wiederholte Tabelle hinzu.  Der Beispielcode für dieses Beispiel sortiert die Zeilen basierend auf der ersten Spalte in der Tabelle, Sie können den Code jedoch ganz einfach so ändern, dass er mit einer beliebigen Spalte funktioniert. 
    
2. Fügen Sie dem Formular ein **Schaltfläche**-Steuerelement hinzu. Der Code zum Sortieren der Tabelle wird dem Ereignishandler für das **Clicked-Ereignis** der Schaltfläche hinzugefügt, Sie können jedoch auch ein anderes Ereignis für diesen Zweck verwenden. 
    
3. Wählen Sie die Schaltfläche aus, klicken Sie auf die Registerkarte **Eigenschaften**, und klicken Sie dann auf **Benutzerdefinierter Code**. Wenn das Formular noch nicht gespeichert wurde, werden Sie zum Speichern aufgefordert. Anschließend wird der Code-Editor mit dem Cursor im Ereignishandler der Schaltfläche geöffnet.
    
4. Fügen Sie den folgenden Code in den Ereignishandler der Schaltfläche ein. Durch den Code werden die Elemente aus der ersten Spalte in einem Array platziert, das Array wird sortiert, und dann wird die Tabelle basierend auf dem sortierten Array neu angeordnet. Bei diesem Code wird angenommen, dass es sich bei den zu sortierenden Daten um Zeichenfolgedaten handelt.
    
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

5. Veröffentlichen Sie Das Formular mithilfe der folgenden Schritte:
    
    1. Klicken Sie auf der Registerkarte **"Veröffentlichen"** in der Backstage auf **SharePoint Server.** 
        
    2. Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**. 
        
       > [!IMPORTANT]
       > Sie müssen ein Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als Sandkastenlösung zu veröffentlichen. 
    
    3. Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.
        
    5. Geben Sie den Namen und die Beschreibungen für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.
        
    6. Klicken Sie auf **Veröffentlichen**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Beispiel 2: Verwalten von Anbietern in einer SharePoint Liste

Dieses Beispiel umfasst die Programmierung für das Microsoft SharePoint Foundation 2010-Objektmodell. Hierzu müssen Sie einen Verweis auf die Microsoft.SharePoint.dll assembly einrichten, die mit einer lizenzierten Kopie von SharePoint Server 2010 installiert ist.
  
Microsoft.SharePoint.Server.dll ist standardmäßig in "C:\Programme\Gemeinsame Dateien\Microsoft Shared\Web Server Extensions\14\ISAPI" installiert. Diese DLL muss in Projekten enthalten sein, in denen Sie für das SharePoint-Objektmodell programmieren. Um einen Verweis auf die Microsoft.SharePoint.dll in einem Visual Studio 2012-Projekt einzurichten, öffnen Sie den **Code-Editor,** und klicken Sie dann im Menü **Extras** auf **Verweis hinzufügen.** Klicken **Sie** im Dialogfeld Verweis hinzufügen auf die Registerkarte **"Durchsuchen",** geben Sie den Speicherort der Microsoft.SharePoint.dll-Datei an, und klicken Sie dann auf **"OK".** Dadurch wird die Microsoft.SharePoint.dll in das Projektverzeichnis kopiert, sodass Sie SharePoint Foundation 2010-Objektmodellmember in Ihrer InfoPath-Lösung verwenden können.
  
### <a name="designing-the-form-and-developing-the-code"></a>Entwerfen des Formulars und Entwickeln des Codes

Aus Code in einem InfoPath-Formular können Sie das SharePoint-Objektmodell verwenden, um Elemente in Nachschlagelisten zu erstellen. Dies ist nützlich, wenn Sie ein Dropdownfeld aus einer SharePoint Liste auffüllen und neue Werte hinzufügen möchten, ohne ein separates Formular zu erstellen. In diesem Beispiel wird ein Kombinationsfeld verwendet, um alle werte anzuzeigen, die sich derzeit in der Liste befinden, und es wird Programmierlogik erstellt, um den Wert der Liste hinzuzufügen, wenn er noch nicht vorhanden ist.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>So erstellen Sie eine Formularvorlage zum Hinzufügen neuer Elemente zu einem Kombinationsfeld, das auf einer SharePoint-Liste basiert

1. Erstellen Sie eine einfache benutzerdefinierte Liste auf einem SharePoint Server 2010-Server, und nennen Sie sie "MyList". Im folgenden Beispiel wird ein **Kombinationsfeld** verwendet, das an das **Feld "Titel"** dieser Liste gebunden ist. 
    
2. Erstellen Sie ein neues **leeres Formular** in InfoPath Designer, fügen Sie ein **Kombinationsfeld-Steuerelement** in Das Formular ein, und benennen Sie das an das Kombinationsfeld gebundene Feld in "myCombo" um.
    
3. Erstellen Sie die Datenverbindung mit der Liste, die zum Auffüllen des Kombinationsfelds verwendet wird, mithilfe der folgenden Schritte:
    
    1. Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Externe Daten** auf die Schaltfläche **Aus SharePoint-Liste**. 
        
    2. Geben Sie die URL der Website ein, die die Liste enthält, und klicken Sie dann auf **Weiter**.
        
    3. Wählen Sie die Liste aus, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie die einzuschließenden Felder aus (in diesem Beispiel Title und ID). Title enthält die Werte zum Nachschlagen. Klicken Sie auf **Weiter**.
        
    5. Klicken Sie auf dem folgenden Bildschirm auf **Weiter**. 
        
    6. Benennen Sie die Datenverbindung LookupList, und klicken Sie dann auf **Fertig stellen**.
    
4. Füllen Sie die Werte im Kombinationsfeld aus der Liste mithilfe der folgenden Schritte auf:
    
    1. Wählen Sie das in Schritt 1 erstellte Kombinationsfeld aus.
        
    2. Klicken Sie auf der Registerkarte **Eigenschaften von Steuerelementtools** des Menübands auf **Auswahlmöglichkeiten bearbeiten**. 
        
    3. Wählen Sie **Auswahl aus einer externen Datenquelle abrufen** aus.
        
    4. Stellen Sie sicher, dass **Datenquelle** auf die in Schritt 2 erstellte Datenverbindung festgelegt ist. 
        
    5. Legen Sie den Wert und den Anzeigenamen auf Title fest.
        
    6. Wählen Sie auf der Registerkarte **"Browserformulare"** **immer** unter **"Postbackeinstellungen"** aus, und klicken Sie dann auf **"OK",** um das Dialogfeld "Eigenschaften" zu schließen. 
    
5. Stellen Sie sicher, dass das Kombinationsfeld weiterhin ausgewählt ist, und klicken Sie dann auf der Registerkarte **"Entwickler"** des Menübands auf **"Ereignis ändern".** 
    
    Wenn das Formular noch nicht gespeichert wurde, werden Sie zum Speichern aufgefordert. Anschließend wird das Code-Editor-Fenster mit dem Cursor im  `myCombo_Changed` Ereignishandler geöffnet. 
    
6. Fügen Sie wie weiter oben in diesem Thema beschrieben einen Verweis auf die Microsoft.SharePoint.dll-Assembly hinzu. Weitere Informationen zum Verweisen auf Microsoft. SharePoint Assembly finden Sie unter [Verwenden von SharePoint-Objektmodellmembern.](how-to-use-sharepoint-object-model-members.md)
    
7. Fügen Sie den folgenden Code in den  `myCombo_Changed` Ereignishandler ein. 
    
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

8. Das vorherige Codebeispiel hängt von der  `GetDomValue` Hilfsfunktion ab. Fügen Sie den folgenden Code für die  `GetDomValue` Hilfsfunktion unterhalb der  `myCombo_Changed` Ereignishandlerfunktion ein. 
    
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

9. Veröffentlichen Sie Das Formular mithilfe der folgenden Schritte:
    
    1. Klicken Sie auf der Registerkarte **"Veröffentlichen"** in der Backstage auf **SharePoint Server.** 
        
    2. Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**. 
        
       > [!IMPORTANT]
       > Sie müssen ein Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als Sandkastenlösung zu veröffentlichen. 
    
    3. Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.
        
    5. Geben Sie den Namen und die Beschreibung für Ihre Formularbibliothek ein, und klicken Sie dann auf **"Weiter".**
        
    6. Klicken Sie auf **Veröffentlichen**.
        
    7. Nachdem das Formular erfolgreich veröffentlicht wurde, öffnen Sie das Formular aus der Formularbibliothek, und fügen Sie einen neuen Wert in das Kombinationsfeld ein, um den Code zu testen. Wenn Sie das Feld myCombo beenden, wird der neue Wert in die liste SharePoint geschrieben. 
    

