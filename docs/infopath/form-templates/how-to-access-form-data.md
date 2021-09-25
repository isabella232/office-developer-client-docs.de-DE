---
title: Zugreifen auf Formulardaten
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form data [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], printing,closing forms [InfoPath 2007],InfoPath 2007, accessing form data,forms [InfoPath 2007], accessing data source,forms [InfoPath 2007], closing,forms [InfoPath 2007], opening,printing [InfoPath 2007], forms,forms [InfoPath 2007],  Erstellen
ms.localizationpriority: medium
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt das Zugreifen auf und Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der XmlForm-Klasse in Verbindung mit der XmlFormCollection-Klasse.
ms.openlocfilehash: 8b54013ee925491f7060dc088975ea65232fe12e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557477"
---
# <a name="access-form-data"></a>Zugreifen auf Formulardaten

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt das Zugreifen auf und Bearbeiten des einem Formular zugrunde liegenden XML-Dokuments durch die Verwendung der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) in Verbindung mit der [XmlFormCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) 
  
Die [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ist einer der nützlichsten Typen im InfoPath-Objektmodell, da sie eine Vielzahl von Eigenschaften und Methoden bereitstellt, die nicht nur mit dem einem Formular zugrunde liegenden XML-Dokument interagieren, sondern auch viele der Aktionen ausführen, die auf der InfoPath-Benutzeroberfläche verfügbar sind. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Übersicht über die XmlFormCollection-Klasse

Die [XmlFormCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler zum Verwalten der in der Auflistung enthaltenen [XmlForm-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[New(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular.  <br/> |
|[New(String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (Überladung 1)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[NewFromFormTemplate(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage ein neues Formular.  <br/> |
|[NewFromFormTemplate(String, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 1)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage und XML-Daten ein neues Formular.  <br/> |
|[NewFromFormTemplate(String, String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 2)  <br/> |Erstellt ein neues Formular basierend auf der angegebenen Formularvorlage mit Daten, die durch ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt angegeben werden.  <br/> |
|[NewFromFormTemplate(String, XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 3)  <br/> |Erstellt ein neues Formular auf Grundlage der angegebenen Formularvorlage mit durch ein **XPathNavigator**-Objekt angegebenen Daten mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Open(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Open(String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (Überladung 1)  <br/> |Öffnet das angegebene Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **XmlForm**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene **XmlForm**-Objekt aus der Auflistung nach Indexwert ab.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Übersicht über die XmlForm-Klasse

Die [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler verwenden können, um mit dem einem Formular zugrunde liegenden XML-Dokument zu interagieren und Aktionen auszuführen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)-Methode  <br/> |Schließt das Formular.  <br/> |
|[GetWorkflowTasks-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTasks**-Auflistung des aktuellen Formulars ab.  <br/> |
|[GetWorkflowTemplates-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTemplates**-Auflistung des aktuellen Formulars ab.  <br/> |
|[MergeForm(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Führt das aktuelle Formular mit dem über den Pfad oder URL angegebenen Formular zusammen.  <br/> |
|[MergeForm(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (Überladung 1)  <br/> |Führt das aktuelle Formular mit dem im Knoten angegebenen Zielformular zusammen. Dies ist der von **XPathNavigator**, der an die Methode übergeben wurde, zurückgegebene Knoten.  <br/> |
|[NotifyHost-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Stellt einen benutzerdefinierten Wert für die Hostanwendung oder ASPX-Seite (Active Server Page Extension) bereit.  <br/> |
|[Print()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird.  <br/> |
|[Print(Boolean)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (Überladung 1)  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird, indem das Dialogfeld **Drucken** angezeigt wird.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)-Methode  <br/> |Speichert das Formular unter dem ihr zurzeit zugeordneten URL (Uniform Resource Locator).  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)-Methode  <br/> |Speichert das Formular unter dem angegebenen URL (Uniform Resource Locator).  <br/> |
|[SetSaveAsDialogFilename-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Legt den Standarddateinamen für das Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Legt den Standardpfad zum Speichern des Formulars mithilfe des Dialogfeldes **Speichern unter** fest.  <br/> |
|[Submit-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Sendet das Formular mithilfe des in der Formularvorlage definierten Sendevorgangs.  <br/> |
|[CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Ruft ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt, das die aktuelle Ansicht des Formulars darstellt.  <br/> |
|[DataConnections-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Ruft ein [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) -Objekt ab, das dem Formular zugeordnet ist.  <br/> |
|[DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Ruft das [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Objekt ab, das dem Formular zugeordnet ist.  <br/> |
|[Dirty-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob die Daten in einem Formular seit dem letzten Speichern geändert wurden.  <br/> |
|[Errors-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Ruft einen Verweis auf die [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) ab, die einem Formular zugeordnet ist.  <br/> |
|[Extension-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Ruft ein [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) für den Zugriff auf die Funktionen und globalen Variablen in der primären Formularcodedatei eines Formulars mithilfe von [System.Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx)ab.  <br/> |
|[FormState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Ruft einen Verweis auf eine Eigenschaftensammlung vom Typ [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) ab, der von browserfähigen Formularen zum Beibehalten von Statusinformationen in allen Sitzungen auf dem Server verwendet werden kann.  <br/> |
|[Host-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Ruft [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) ab, mit Zugriffsmöglichkeit auf das Objektmodell der Hostanwendung mittels Code, das in einer gehosteten Instanz von InfoPath ausgeführt wird.  <br/> |
|[Hosted-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Ruft ab, ob InfoPath in einer anderen Anwendung als Steuerelement gehostet wird.  <br/> |
|[HostName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Ruft den Namen der Anwendung ab, mit der InfoPath als Steuerelement gehostet wird.  <br/> |
|[MainDataSource-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Ruft ein [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt, das die Hauptdatenquelle des Formulars darstellt.  <br/> |
|[NamespaceManager-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Ruft einen Verweis auf ein [XmlNamespaceManager -Objekt](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) ab, das zum Auflösen, Hinzufügen oder Entfernen von Namespaces verwendet werden kann, die im Formular verwendet werden.  <br/> |
|[New-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular neu ist.  <br/> |
|[Permission-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Ruft einen Verweis auf ein [Permission -Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) ab, das dem Formular zugeordnet ist.  <br/> |
|[QueryDataConnection-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Ruft einen Verweis auf das [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) -Objekt, das die Datenverbindung darstellt, die dem Formular zugeordnet ist.  <br/> |
|[ReadOnly-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob eine Formularvorlage schreibgeschützt oder gesperrt ist.  <br/> |
|[Recovered-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular zuletzt mithilfe eines AutoWiederherstellen-Speichervorgangs gespeichert wurde.  <br/> |
|[Signed-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular mithilfe digitaler Signaturen digital signiert wurde.  <br/> |
|[SignedDataBlocks-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Ruft einen Verweis auf die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Auflistung ab, die einem Formular zugeordnet ist.  <br/> |
|[TaskPanes-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Ruft einen Verweis auf die [TaskPaneCollection ab,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) die einer Formularvorlage zugeordnet ist.  <br/> |
|[Template-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Ruft einen Verweis auf das [FormTemplate-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) ab, das das Manifest (XSF) der Formularvorlage darstellt, die dem Formular zugeordnet ist.  <br/> |
|[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)-Eigenschaft  <br/> |Ruft den URI (Uniform Resource Identifier) eines Formulars ab.  <br/> |
|[UserRole-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Ruft den aktuellen Benutzer des Rollennamens im Formular ab oder legt diesen fest.  <br/> |
|[ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Ruft einen Verweis auf das [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Objekt ab, das der Formularvorlage zugeordnet ist.  <br/> |
|[XmlLang-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Ruft den Wert des **xml:lang**-Attributs im dem Formular zugrunde liegenden XML-Dokument ab.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Verwenden der XmlFormCollection-Klasse

Der Zugriff auf die **XmlFormCollection-Klasse** erfolgt über die [XmlForms-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) der [Application-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) In einer Formularvorlage mit verwaltetem Code, die mithilfe des von den Mitgliedern der Microsoft.Office bereitgestellten Objektmodells erstellt [wurde. InfoPath-Namespace,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) you can use the **this** (C#) or **Me** (Visual Basic) keyword in your form code to access the **Application** class and its members. 
  
Im folgenden Beispiel wird die **XmlForms-Eigenschaft** der **Application-Klasse** verwendet, um eine Objektvariable namens "myForms" zu erstellen, die auf das **XDocumentsCollection-Objekt** der aktuell ausgeführten Instanz von InfoPath verweist. Diese Variable wird dann zum Anzeigen der Anzahl von geöffneten Formularen verwendet. 
  
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

In einer Formularvorlage mit verwaltetem Code, die mithilfe des von den Mitgliedern der Microsoft.Office bereitgestellten Objektmodells erstellt [wurde. InfoPath-Namespace,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) you can use the **this** (C#) or **Me** (Visual Basic) keyword in your form code to access the members of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class directly (without requiring an object variable that establishes a reference to the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class). 
  
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

Eine wichtige Eigenschaft der **XmlForm**-Klasse hinsichtlich Formulardaten ist die **MainDataSource**-Eigenschaft. Diese Eigenschaft gibt einen Verweis auf ein [DataSource-Objekt zurück,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) das die zugrunde liegenden XML-Daten des aktuellen Formulars darstellt, die auch als Hauptdatenquelle oder primäre Datenquelle des Formulars bezeichnet werden. Die **DataSource-Klasse** stellt die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) bereit, die ein [XPathNavigator-Objekt](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) erstellt, das sich am Stamm des dem Formular zugrunde liegenden XML-Dokuments befindet. Die Eigenschaften und Methoden der **XPathNavigator**-Klasse können dann verwendet werden, um in den zugrunde liegenden XML-Daten des Formulars zu navigieren und sie zu bearbeiten. 
  
Im folgenden Beispiel wird die **MainDataSource**-Eigenschaft der **XmlForm**-Klasse zum Erstellen eines **XPathNavigator**-Objekts verwendet, das im Stammknoten der Hauptdatenquelle des Formulars positioniert ist. Die **OuterXml-Eigenschaft** der **XPathNavigator-Klasse** wird dann verwendet, um den gesamten Inhalt des einem Formular zugrunde liegenden XML-Dokuments zurückzugeben und anzuzeigen. 
  
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
  
Weitere Informationen zur **XPathNavigator-Klasse** in der Geschäftslogik einer InfoPath-Formularvorlage finden Sie unter [Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Zugreifen auf Daten über die Formularvorlagendatei eines Formulars

Auf Informationen zu einem Formular zugeordnete Formularvorlage, einschließlich der Formulardefinitionsdatei (XSF) und der enthaltenen XML-Daten kann auch mithilfe der **XmlForm**-Klasse zugegriffen werden. Auf diese Informationen wird mithilfe der [Template-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) zugegriffen, die einen Verweis auf ein [FormTemplate-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) zurückgibt, das die dem aktuellen Formular zugeordnete Formularvorlage darstellt. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die **Vorlagenklasse** verfügbar sind, z. B. den Speicherort des Uniform Resource Identifier (URI) (unter Verwendung der [Uri-Eigenschaft),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) den Cachebezeichner (mithilfe der [CacheId-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) und die Versionsnummer (mithilfe der [Version-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) Im nächsten Meldungsfeld wird die [Manifest-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) der **Template-Klasse** verwendet, um ein **XPathNavigator-Objekt** zu erstellen, das zum Anzeigen des Quell-XML der Formulardefinitionsdatei (XSF) verwendet wird. 
  
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


