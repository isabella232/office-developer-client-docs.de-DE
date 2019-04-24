---
title: Access-Formulardaten
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- Formulardaten [InfoPath 2007], Formulare [InfoPath 2007], Zugriff auf Eigenschaften, Formularvorlagen [InfoPath 2007], zugreifen auf Eigenschaften, Öffnen von Formularen [InfoPath 2007], Drucken von Formularen [InfoPath 2007], Formulare [InfoPath 2007], drucken, schließen von Formularen [InfoPath 2007], InfoPath 2007, Zugriff auf Formulardaten, Formulare [InfoPath 2007], Zugriff auf Datenquelle, Formulare [InfoPath 2007], schließen, Formulare [InfoPath 2007], öffnen, drucken [InfoPath 2007], Formulare, Formulare [InfoPath 2007], erstellen
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der XmlForm-Klasse in Verbindung mit der xmlFormcollection-Klasse.
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300210"
---
# <a name="access-form-data"></a>Access-Formulardaten

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und das Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der XmlForm-Klasse in Verbindung mit der xmlFormcollection-Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) 
  
Die [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse ist einer der nützlichsten Typen im InfoPath-Objektmodell, da Sie eine Vielzahl von Eigenschaften und Methoden bereitstellt, die nicht nur mit dem einem Formular zugrunde LIEGENden XML-Dokument interagieren, sondern auch viele der Aktionen ausführen, die in der InfoPath-Benutzeroberfläche. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Übersicht über die XmlFormCollection-Klasse

Die [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) XmlFormCollection-Klasse stellt die folgenden Methoden und Eigenschaften bereit, mit denen Entwickler die in [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) der Auflistung enthaltenen XmlForm-Objekte verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[New (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) -Methode  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular.  <br/> |
|[New (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) -Methode (Overload 1)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[NewFromFormTemplate (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode  <br/> |Erstellt basierend auf der angegebenen Formularvorlage ein neues Formular.  <br/> |
|[NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Overload 1)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage und XML-Daten ein neues Formular.  <br/> |
|[NewFromFormTemplate (String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Overload 2)  <br/> |Erstellt ein neues Formular basierend auf der angegebenen Formularvorlage mit Daten, die durch ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt angegeben werden.  <br/> |
|[NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Overload 3)  <br/> |Erstellt ein neues Formular auf Grundlage der angegebenen Formularvorlage mit durch ein **XPathNavigator**-Objekt angegebenen Daten mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Open (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) -Methode  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Open (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) -Methode (Overload 1)  <br/> |Öffnet das angegebene Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **XmlForm**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene **XmlForm**-Objekt aus der Auflistung nach Indexwert ab.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Übersicht über die XmlForm-Klasse

Die [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) XmlForm-Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler verwenden können, um mit dem einem Formular zugrunde liegenden XML-Dokument zu interagieren und Aktionen auszuführen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)-Methode  <br/> |Schließt das Formular.  <br/> |
|[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) -Methode  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTasks**-Auflistung des aktuellen Formulars ab.  <br/> |
|[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) -Methode  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTemplates**-Auflistung des aktuellen Formulars ab.  <br/> |
|[MergeForm (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode  <br/> |Führt das aktuelle Formular mit dem über den Pfad oder URL angegebenen Formular zusammen.  <br/> |
|[MergeForm (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode (Overload 1)  <br/> |Führt das aktuelle Formular mit dem im Knoten angegebenen Zielformular zusammen. Dies ist der von **XPathNavigator**, der an die Methode übergeben wurde, zurückgegebene Knoten.  <br/> |
|[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) -Methode  <br/> |Stellt einen benutzerdefinierten Wert für die Hostanwendung oder ASPX-Seite (Active Server Page Extension) bereit.  <br/> |
|[Print ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) -Methode  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird.  <br/> |
|[Print (Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) -Methode (Overload 1)  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird, indem das Dialogfeld **Drucken** angezeigt wird.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)-Methode  <br/> |Speichert das Formular unter dem ihr zurzeit zugeordneten URL (Uniform Resource Locator).  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)-Methode  <br/> |Speichert das Formular unter dem angegebenen URL (Uniform Resource Locator).  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) -Methode  <br/> |Legt den Standarddateinamen für das Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) -Methode  <br/> |Legt den Standardpfad zum Speichern des Formulars mithilfe des Dialogfeldes **Speichern unter** fest.  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) -Methode  <br/> |Sendet das Formular mithilfe des in der Formularvorlage definierten Sendevorgangs.  <br/> |
|[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft  <br/> |Ruft ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt ab, das die aktuelle Ansicht des Formulars darstellt.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) DataConnections-Eigenschaft  <br/> |Ruft ein [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) DataConnectionCollection-Objekt ab, das dem Formular zugeordnet ist.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) DataSources-Eigenschaft  <br/> |Ruft das [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) DataSourceCollection-Objekt ab, das dem Formular zugeordnet ist.  <br/> |
|[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob die Daten in einem Formular seit dem letzten Speichern geändert wurden.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) ab, das einem Formular zugeordnet ist.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) -Eigenschaft  <br/> |Ruft ein [System. Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) für den Zugriff auf die Funktionen und globalen Variablen ab, die in der primären Formular Codedatei eines Formulars mithilfe von [System. Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx)enthalten sind.  <br/> |
|[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf eine Eigenschaftensammlung vom Typ [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) ab, der von browserfähigen Formularen zum Beibehalten von Statusinformationen in allen Sitzungen auf dem Server verwendet werden kann.  <br/> |
|[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) -Eigenschaft  <br/> |Ruft [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) ab, mit Zugriffsmöglichkeit auf das Objektmodell der Hostanwendung mittels Code, das in einer gehosteten Instanz von InfoPath ausgeführt wird.  <br/> |
|[Hosted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) -Eigenschaft  <br/> |Ruft ab, ob InfoPath in einer anderen Anwendung als Steuerelement gehostet wird.  <br/> |
|[Hostname](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) -Eigenschaft  <br/> |Ruft den Namen der Anwendung ab, mit der InfoPath als Steuerelement gehostet wird.  <br/> |
|[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft  <br/> |Ruft ein [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt ab, das die Hauptdatenquelle des Formulars darstellt.  <br/> |
|[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) -Objekt ab, das zum Auflösen, hinzufügen oder Entfernen von im Formular verwendeten Namespaces verwendet werden kann.  <br/> |
|[Neue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular neu ist.  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) -Objekt ab, das dem Formular zugeordnet ist.  <br/> |
|[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) -Objekt ab, das die dem Formular zugeordnete Datenverbindung darstellt.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob eine Formularvorlage schreibgeschützt oder gesperrt ist.  <br/> |
|[Wiederhergestellte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular zuletzt mithilfe eines AutoWiederherstellen-Speichervorgangs gespeichert wurde.  <br/> |
|[Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular mithilfe digitaler Signaturen digital signiert wurde.  <br/> |
|[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Auflistung ab, die einem Formular zugeordnet ist.  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) ab, die einer Formularvorlage zugeordnet ist.  <br/> |
|[Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [Form Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) -Objekt ab, das das Manifest (XSF) der Formularvorlage darstellt, die dem Formular zugeordnet ist.  <br/> |
|[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)-Eigenschaft  <br/> |Ruft den URI (Uniform Resource Identifier) eines Formulars ab.  <br/> |
|[Userrole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) -Eigenschaft  <br/> |Ruft den aktuellen Benutzer des Rollennamens im Formular ab oder legt diesen fest.  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Objekt ab, das der Formularvorlage zugeordnet ist.  <br/> |
|[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) -Eigenschaft  <br/> |Ruft den Wert des **xml:lang**-Attributs im dem Formular zugrunde liegenden XML-Dokument ab.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Verwenden der XmlFormCollection-Klasse

Der **** Zugriff auf die XmlFormCollection-Klasse erfolgt über die XmlForms-Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) In einer Formularvorlage mit verwaltetem Code, die mit dem von den Membern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellten Objektmodell erstellt wurde, können Sie das Schlüsselwort **this** (C#) oder **Me** (Visual Basic) im Formularcode verwenden, um auf die Anwendung zuzugreifen. ** **Klasse und ihre Member. 
  
Im folgenden Beispiel wird die **** XmlForms-Eigenschaft der **Application** -Klasse zum Erstellen einer Objektvariablen mit dem Namen myForms verwendet, die auf das **XDocumentsCollection** -Objekt der aktuell laufenden InfoPath-Instanz verweist. Diese Variable wird dann zum Anzeigen der Anzahl von geöffneten Formularen verwendet. 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

Die Variable myForms kann dann auch zum Erstellen neuer Formulare (mithilfe der Methoden **New** oder **NewFromTemplate**) oder zum Öffnen vorhandener Formulare (mithilfe einer der **Open**-Methoden) verwendet werden. 
  
## <a name="using-the-xmlform-class"></a>Verwenden der XmlForm-Klasse

In einer Formularvorlage mit verwaltetem Code, die mit dem von den Membern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellten Objektmodell erstellt wurde, können Sie das Schlüsselwort **this** (C#) oder **Me** (Visual Basic) im Formularcode verwenden, um auf die Member [der XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse direkt (ohne eine Objektvariable zu erfordern, die einen Verweis auf die [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse herstellt). 
  
### <a name="accessing-a-forms-property-values"></a>Zugreifen auf die Eigenschaftenwerte eines Formulars

Im folgenden Beispiel wird das Schlüsselwort **this** oder **Me** für den Zugriff auf die Eigenschaften **New**, **ReadOnly**, **Signed** und **Uri** der **XmlForm**-Klasse und zum Anzeigen der zurückgegebenen Werte für das aktuelle Formular in einem Meldungsfeld verwendet. 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>Zugreifen auf die Datenquelle eines Formulars

Eine wichtige Eigenschaft der **XmlForm**-Klasse hinsichtlich Formulardaten ist die **MainDataSource**-Eigenschaft. Diese Eigenschaft gibt einen Verweis auf ein [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt zurück, das die zugrunde liegenden XML-Daten des aktuellen Formulars darstellt, das auch als Haupt-oder primäre Datenquelle des Formulars bezeichnet wird. Die **DataSource** -Klasse stellt [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) die CreateNavigator-Methode bereit, die ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt am Stamm des dem Formular zugrunde liegenden XML-Dokuments positioniert. Die Eigenschaften und Methoden der **XPathNavigator**-Klasse können dann verwendet werden, um in den zugrunde liegenden XML-Daten des Formulars zu navigieren und sie zu bearbeiten. 
  
Im folgenden Beispiel wird die **MainDataSource**-Eigenschaft der **XmlForm**-Klasse zum Erstellen eines **XPathNavigator**-Objekts verwendet, das im Stammknoten der Hauptdatenquelle des Formulars positioniert ist. Die **OuterXml** -Eigenschaft der **XPathNavigator** -Klasse wird dann verwendet, um den gesamten Inhalt des einem Formular zuGRUNDE liegenden XML-Dokuments zurückzugeben und anzuzeigen. 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> Da InfoPath die **MainDataSource**-Eigenschaft als Standardeigenschaft für das **XmlForm**-Objekt behandelt, auf das zugegriffen wird, wenn das Schlüsselwort **this** oder **Me** verwendet wird, können Sie sie in der zum Erstellen des **XPathNavigator**-Objekts verwendeten Codezeile auslassen. 
  
Weitere Informationen zur **XPathNavigator** -Klasse in der Geschäftslogik einer InfoPath-Formularvorlage finden Sie unter [Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)".
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Zugreifen auf Daten über die Formularvorlagendatei eines Formulars

Auf Informationen zu einem Formular zugeordnete Formularvorlage, einschließlich der Formulardefinitionsdatei (XSF) und der enthaltenen XML-Daten kann auch mithilfe der **XmlForm**-Klasse zugegriffen werden. Auf diese Informationen wird mithilfe der [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) -Eigenschaft zugegriffen, die einen Verweis auf ein [Form Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) -Objekt zurückgibt, das die dem aktuellen Formular zugeordnete Formularvorlage darstellt. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die **Template** -Klasse verfügbar sind, beispielsWEISE den URI-Speicherort (Uniform Resource Identifier) (mit der [URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) -Eigenschaft), den Cachebezeichner (mit der Cache-ID [ ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx)-Eigenschaft) und die Versionsnummer (mit der [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) -Eigenschaft). Im nächsten Meldungsfeld wird die [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) -Eigenschaft der **Template** -Klasse verwendet, um ein **XPathNavigator** -Objekt zu erstellen, das zum Anzeigen der Quell-XML der Formulardefinitionsdatei (XSF) verwendet wird. 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


