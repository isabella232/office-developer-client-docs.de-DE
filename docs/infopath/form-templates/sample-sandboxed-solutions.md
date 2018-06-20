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
# <a name="sample-sandboxed-solutions"></a>Beispiele für sandkastenlösungen

InfoPath-Formulare mit verwaltetem Code können aus dem InfoPath-Designer mit der SharePoint-Infrastruktur sandkastenlösung veröffentlicht werden. Dieses Thema enthält zwei Beispiele, in denen der Art der Code zeigt an, dass Sie in einer InfoPath-sandkastenlösung und zum Veröffentlichen der Formularvorlage schreiben können.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>In Beispiel 1: Sortieren von Daten in einem Bestellformular

Eine nützliche Aufgabe, die Sie ausführen können, mithilfe von Code in einem InfoPath-Formular ist zum Sortieren von Daten in einer wiederholten Tabelle. Zu diesem Zweck ordnet der Code die Knoten in der zugrunde liegenden XML-Dokument, das im InfoPath-Formular angezeigt wird. Obwohl das in diesem Thema beschriebene Szenario für die Veröffentlichung direkt in InfoPath als sandkastenlösung gerichtet ist, können sie auch als vom Administrator genehmigten Formularvorlage bereitgestellt werden.
  
Stellen Sie vor Beginn sicher, dass die folgenden Anforderungen erfüllt sind.
  
- Sie sind Administrator einer Websitesammlung auf der SharePoint Server 2010 oder SharePoint Foundation 2010-Website, in dem Sie das Formular veröffentlichen möchten.
    
- Überprüfen Sie mit dem Farmadministrator, um sicherzustellen, dass der Microsoft SharePoint Foundation Sandboxed Code-Dienst auf dem Server ausgeführt wird. Weitere Informationen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).
    
- Die Programmiersprache, die Sie für die Formularvorlage ausgewählt haben ist entweder **c#** oder **Visual Basic** nach dem ohne einen beliebigen Versionsnamen der früheren. Die InfoPath 2007-kompatiblen und InfoPath 2003-kompatiblen Versionen der Programmiersprachen und Objektmodelle werden für sandkastenlösungen nicht unterstützt. Weitere Informationen zum Angeben der Programmiersprache finden Sie unter [Entwickeln mit Visual Studio](how-to-develop-with-visual-studio.md).
    
Führen Sie die folgenden Schritte aus, um eine Formularvorlage zu erstellen, die die Daten in einem **Wiederholte Tabelle** -Steuerelement im Formular sortiert. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>So erstellen Sie eine Formularvorlage zum programmatischen Sortieren von Daten im Formular

1. Erstellen Sie eine neue Formularvorlage im InfoPath-Designer, und fügen Sie ein Steuerelement **Wiederholte Tabelle** auf das Formular. Der Beispielcode in diesem Beispiel werden die Zeilen basierend auf der ersten Spalte in der Tabelle sortiert, aber Sie können den Code zum Arbeiten mit einer beliebigen Spalte ganz einfach ändern. 
    
2. Fügen Sie dem Formular ein **Button** -Steuerelement. Der Code zum Sortieren der Tabelle wird der Ereignishandler für die Schaltfläche **Clicked** -Ereignis hinzugefügt werden, aber Sie können auch ein anderes Ereignis für diesen Zweck verwenden. 
    
3. Wählen Sie die Schaltfläche aus, klicken Sie auf der Registerkarte **Eigenschaften** , und klicken Sie dann auf **Benutzerdefinierter Code**. Wenn das Formular noch nicht gespeichert wurde, Sie werden aufgefordert, ihn zu speichern, und klicken Sie dann im Code-Editor wird mit dem Mauszeiger in-Ereignishandler der Schaltfläche geöffnet.
    
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

5. Veröffentlichen Sie das Formular mithilfe der folgenden Schritte aus:
    
    1. Klicken Sie auf der Registerkarte **Veröffentlichen** in der Backstage-Ansicht auf **SharePoint Server** . 
        
    2. Geben Sie die URL der SharePoint-Website veröffentlichen, und klicken Sie dann auf **Weiter**. 
        
       > [!IMPORTANT]
       > Sie müssen ein Websitesammlungsadministrator auf dieser Website zum Veröffentlichen dieser Formularvorlage als sandkastenlösung sein. 
    
    3. Wählen Sie **Formularbibliothek**aus, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie **eine neue Formularbibliothek erstellen**aus, und klicken Sie dann auf **Weiter**.
        
    5. Geben Sie den Namen und eine Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.
        
    6. Klicken Sie auf **Veröffentlichen**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Beispiel 2: Verwalten von Anbietern in einer SharePoint-Liste

In diesem Beispiel umfasst Programmieren mit dem Microsoft SharePoint Foundation 2010-Objektmodell. Zu diesem Zweck müssen Sie einen Verweis auf die Microsoft.SharePoint.dll-Assembly einrichten, die mit eine lizenzierte Version von SharePoint Server 2010 installiert wird.
  
Microsoft.SharePoint.Server.dll wird in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI standardmäßig installiert. Diese DLL muss in Projekten, in dem Programmieren der SharePoint-Objektmodell, enthalten sein. Wenn Sie einen Verweis auf die Microsoft.SharePoint.dll in einem Projekt auf Visual Studio 2012 eingerichtet haben, öffnen Sie den **Code-Editor**, und klicken Sie dann im Menü **Extras** auf **Verweis hinzufügen** . Klicken Sie im Dialogfeld **Verweis hinzufügen** klicken Sie auf die Registerkarte **Durchsuchen** , geben Sie den Speicherort der Microsoft.SharePoint.dll-Datei, und klicken Sie dann auf **OK**. Dadurch wird die Microsoft.SharePoint.dll in das Projektverzeichnis kopiert, damit Sie SharePoint Foundation 2010 Objektmodellelemente in InfoPath-Lösung verwenden können.
  
### <a name="designing-the-form-and-developing-the-code"></a>Das Formular entwerfen und Entwickeln des Codes

Über Code in einem InfoPath-Formular können Sie das SharePoint-Objektmodell verwenden, Erstellen von Elementen in Nachschlagelisten. Dies ist nützlich, wenn Sie ein Dropdown-Listenfeld aus einer SharePoint-Liste füllen und neue Werte es hinzufügen, ohne zu ein gesonderten Formular erstellen möchten. In diesem Beispiel wird ein Kombinationsfeld verwendet, um alle der Werte, die derzeit in der Liste angezeigt und erstellt die Programmierlogik der Wert der Liste hinzu, wenn er nicht bereits vorhanden ist.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>So erstellen Sie eine Formularvorlage zum Hinzufügen neuer Elemente zu einem Kombinationsfeld, das auf einer SharePoint-Liste basiert

1. Erstellen Sie eine einfache benutzerdefinierte Liste auf einer SharePoint Server 2010-Server, und nennen Sie es MyList. Im folgenden Beispiel wird ein **Kombinationsfeld** an das Feld **Titel** dieser Liste gebunden. 
    
2. Erstellen Sie ein neues **Leeres Formular** im InfoPath-Designer, fügen Sie ein **Kombinationsfeld** -Steuerelement auf Ihrem Formular ein, und benennen Sie das Feld, an das Kombinationsfeld, um in MyCombo gebunden.
    
3. Herstellen der Verbindungs zu der Liste, die zum Auffüllen des Kombinationsfelds mit den folgenden Schritten verwendet werden:
    
    1. Klicken Sie auf der Registerkarte **Daten** auf Schaltfläche in der Gruppe **Externe Daten** **Aus SharePoint-Liste** . 
        
    2. Geben Sie die URL für die Website, die die Liste enthält, und klicken Sie dann auf **Weiter**.
        
    3. Wählen Sie aus der Liste, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie die Felder, die Sie aufnehmen möchten, für die in diesem Beispiel wird, wählen Sie Titel und die gleiche ID. Titel enthält die Werte für die Suche. Klicken Sie auf **Weiter**.
        
    5. Klicken Sie auf dem folgenden Bildschirm auf **Weiter** . 
        
    6. Nennen Sie die Datenverbindung LookupList, und klicken Sie dann auf **Fertig stellen**.
    
4. Füllen Sie die Werte im Kombinationsfeld aus der Liste mit den folgenden Schritten:
    
    1. Wählen Sie das in Schritt 1 erstellte Kombinationsfeld aus.
        
    2. Klicken Sie auf der Registerkarte **Eigenschaften von Tools** des Menübands auf **Auswahlmöglichkeiten bearbeiten** . 
        
    3. Wählen Sie **Auswahl aus einer externen Datenquelle abrufen**.
        
    4. Stellen Sie sicher, dass **Datenquelle** auf die Datenverbindung festgelegt ist, die Sie in Schritt 2 erstellt haben. 
        
    5. Legen Sie den Wert und den Anzeigenamen auf Title fest.
        
    6. Klicken Sie auf der Registerkarte **browserformularen** **immer** unter **Postback Einstellungen**wählen Sie aus, und klicken Sie dann auf **OK** , um das Dialogfeld Eigenschaften zu schließen. 
    
5. Stellen Sie sicher, dass im Kombinationsfeld noch ausgewählt ist, und klicken Sie dann auf der Registerkarte **Entwicklertools** des Menübands auf **Ausgelöstes Ereignis** . 
    
    Wenn das Formular noch nicht gespeichert ist, werden Sie aufgefordert, zu speichern. Und klicken Sie dann Code-Editor-Fenster wird geöffnet, mit dem Mauszeiger in der `myCombo_Changed` -Ereignishandler. 
    
6. Fügen Sie wie weiter oben in diesem Thema beschrieben einen Verweis auf die Microsoft.SharePoint.dll-Assembly hinzu. Weitere Informationen zum Verweisen auf die Microsoft.SharePoint-Assembly finden Sie unter [SharePoint-Objektmodellmember verwenden](how-to-use-sharepoint-object-model-members.md).
    
7. Fügen Sie den folgenden Code in die `myCombo_Changed` -Ereignishandler. 
    
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

8. Im vorherigen Codebeispiel hängt von der `GetDomValue` Hilfsfunktion. Fügen Sie den folgenden Code für die `GetDomValue` Hilfsfunktion unten die `myCombo_Changed` -Ereignishandlerfunktion. 
    
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

9. Veröffentlichen Sie das Formular mithilfe der folgenden Schritte aus:
    
    1. Klicken Sie auf der Registerkarte **Veröffentlichen** in der Backstage-Ansicht auf **SharePoint Server** . 
        
    2. Geben Sie die URL der SharePoint-Website veröffentlichen, und klicken Sie dann auf **Weiter**. 
        
       > [!IMPORTANT]
       > Sie müssen ein Websitesammlungsadministrator auf dieser Website zum Veröffentlichen dieser Formularvorlage als sandkastenlösung sein. 
    
    3. Wählen Sie **Formularbibliothek**aus, und klicken Sie dann auf **Weiter**.
        
    4. Wählen Sie **eine neue Formularbibliothek erstellen**aus, und klicken Sie dann auf **Weiter**.
        
    5. Geben Sie den Namen und eine Beschreibung für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.
        
    6. Klicken Sie auf **Veröffentlichen**.
        
    7. Nachdem das Formular erfolgreich veröffentlicht wurde, öffnen Sie das Formular in der Formularbibliothek, und fügen Sie einen neuen Wert in das Kombinationsfeld zum Testen des Codes. Wenn Sie das Feld in MyCombo beenden, wird der neue Wert in der SharePoint-Liste geschrieben werden. 
    

