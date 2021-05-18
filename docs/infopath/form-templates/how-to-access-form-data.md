---
title: Zugreifen auf Formulardaten
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- formulardaten [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], Drucken,Schließen von Formularen [InfoPath 2007],InfoPath 2007, Zugreifen auf Formulardaten,Formulare [InfoPath 2007], Zugreifen auf Datenquelle,Formulare [InfoPath 2007], Schließen,Formulare [InfoPath 2007], Öffnen,Drucken [InfoPath 2007], Formulare,Formulare [InfoPath 2007], Erstellen,Drucken [InfoPath 2007], Formulare [InfoPath 2007], Erstellen
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff und die Bearbeitung des einem Formular zugrunde liegenden XML-Dokuments mithilfe der XmlForm-Klasse in Verbindung mit der XmlFormCollection-Klasse.
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300210"
---
# <a name="access-form-data"></a>Zugreifen auf Formulardaten

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es häufig notwendig, programmgesteuert auf Informationen zu dem dem Formular zugrunde liegenden XML-Dokument zuzugreifen, auf die Daten zuzugreifen, die das XML-Dokument enthält, oder Aktionen im XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff und die Bearbeitung des einem Formular zugrunde liegenden XML-Dokuments mithilfe der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) in Verbindung mit der [XmlFormCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) 
  
Die [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ist einer der nützlichsten Typen im InfoPath-Objektmodell, da sie eine Vielzahl von Eigenschaften und Methoden bietet, die nicht nur mit dem einem Formular zugrunde liegenden XML-Dokument interagieren, sondern auch viele der Aktionen ausführen, die auf der InfoPath-Benutzeroberfläche verfügbar sind. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Übersicht über die XmlFormCollection-Klasse

Die [XmlFormCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) stellt die folgenden Methoden und Eigenschaften zur Verfügung, die Formularentwickler zum Verwalten der [xmlForm-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) verwenden können, die die Auflistung enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[New(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular.  <br/> |
|[New(String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (Überladung 1)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[NewFromFormTemplate(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage ein neues Formular.  <br/> |
|[NewFromFormTemplate(String, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 1)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage und XML-Daten ein neues Formular.  <br/> |
|[NewFromFormTemplate(String, String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 2)  <br/> |Erstellt ein neues Formular basierend auf der angegebenen Formularvorlage mit Daten, die von einem [XPathNavigator-Objekt angegeben](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) werden.  <br/> |
|[NewFromFormTemplate(String, XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Überladung 3)  <br/> |Erstellt ein neues Formular auf Grundlage der angegebenen Formularvorlage mit durch ein **XPathNavigator**-Objekt angegebenen Daten mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Open(String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Open(String, XmlFormOpenMode)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (Überladung 1)  <br/> |Öffnet das angegebene Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **XmlForm**-Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene **XmlForm**-Objekt aus der Auflistung nach Indexwert ab.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Übersicht über die XmlForm-Klasse

Die [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) bietet die folgenden Methoden und Eigenschaften, mit denen Formularentwickler mit dem einem Formular zugrunde liegenden XML-Dokument interagieren und Aktionen ausführen können. 
  
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
|[CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Ruft ein [View-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) ab, das die aktuelle Ansicht des Formulars darstellt.  <br/> |
|[DataConnections-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Ruft ein [DataConnectionCollection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) ab, das dem Formular zugeordnet ist.  <br/> |
|[DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Ruft das [dataSourceCollection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) ab, das dem Formular zugeordnet ist.  <br/> |
|[Dirty-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob die Daten in einem Formular seit dem letzten Speichern geändert wurden.  <br/> |
|[Errors-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Ruft einen Verweis auf die [FormErrorCollection ab,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) die einem Formular zugeordnet ist.  <br/> |
|[Extension-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Ruft ein [System.Object für](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) den Zugriff auf die Funktionen und globalen Variablen in der primären Formularcodedatei eines Formulars mithilfe von [System.Reflection ab.](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx)  <br/> |
|[FormState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Ruft einen Verweis auf eine Eigenschaftensammlung vom Typ [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) ab, der von browserfähigen Formularen zum Beibehalten von Statusinformationen in allen Sitzungen auf dem Server verwendet werden kann.  <br/> |
|[Host-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Ruft [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) ab, mit Zugriffsmöglichkeit auf das Objektmodell der Hostanwendung mittels Code, das in einer gehosteten Instanz von InfoPath ausgeführt wird.  <br/> |
|[Hosted-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Ruft ab, ob InfoPath in einer anderen Anwendung als Steuerelement gehostet wird.  <br/> |
|[HostName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Ruft den Namen der Anwendung ab, mit der InfoPath als Steuerelement gehostet wird.  <br/> |
|[MainDataSource-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Ruft ein [DataSource-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) ab, das die Hauptdatenquelle des Formulars darstellt.  <br/> |
|[NamespaceManager-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Ruft einen Verweis auf ein [XmlNamespaceManager-Objekt ab,](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) das zum Auflösen, Hinzufügen oder Entfernen von Im Formular verwendeten Namespaces verwendet werden kann.  <br/> |
|[Neue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular neu ist.  <br/> |
|[Permission-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Ruft einen Verweis auf ein [Permission-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) ab, das dem Formular zugeordnet ist.  <br/> |
|[QueryDataConnection-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Ruft einen Verweis auf das [DataConnection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) ab, das die Dem Formular zugeordnete Datenverbindung darstellt.  <br/> |
|[ReadOnly-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob eine Formularvorlage schreibgeschützt oder gesperrt ist.  <br/> |
|[Wiederhergestellte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular zuletzt mithilfe eines AutoWiederherstellen-Speichervorgangs gespeichert wurde.  <br/> |
|[Signed-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular mithilfe digitaler Signaturen digital signiert wurde.  <br/> |
|[SignedDataBlocks-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Ruft einen Verweis auf die [SignedDataBlockCollection-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) ab, die einem Formular zugeordnet ist.  <br/> |
|[TaskPanes-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Ruft einen Verweis auf [die TaskPaneCollection ab,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) die einer Formularvorlage zugeordnet ist.  <br/> |
|[Template-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Ruft einen Verweis auf das [FormTemplate-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) ab, das das Manifest (XSF) der dem Formular zugeordneten Formularvorlage darstellt.  <br/> |
|[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)-Eigenschaft  <br/> |Ruft den URI (Uniform Resource Identifier) eines Formulars ab.  <br/> |
|[UserRole-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Ruft den aktuellen Benutzer des Rollennamens im Formular ab oder legt diesen fest.  <br/> |
|[ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Ruft einen Verweis auf das [ViewInfoCollection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) ab, das der Formularvorlage zugeordnet ist.  <br/> |
|[XmlLang-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Ruft den Wert des **xml:lang**-Attributs im dem Formular zugrunde liegenden XML-Dokument ab.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Verwenden der XmlFormCollection-Klasse

Auf **die XmlFormCollection-Klasse** wird über die [XmlForms-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zugegriffen. In einer Formularvorlage für verwalteten Code, die mithilfe des objektmodells erstellt wurde, das von den Mitgliedern der [Microsoft.Office. InfoPath-Namespace,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) können Sie das Schlüsselwort this **(C#)** oder **Me** (Visual Basic) im Formularcode verwenden, um auf die **Application-Klasse** und ihre Member zu zugreifen. 
  
Im folgenden Beispiel wird die **XmlForms-Eigenschaft** der **Application-Klasse** verwendet, um eine Objektvariable mit dem Namen myForms zu erstellen, die auf das **XDocumentsCollection-Objekt** der derzeit ausgeführten Instanz von InfoPath verweist. Diese Variable wird dann zum Anzeigen der Anzahl von geöffneten Formularen verwendet. 
  
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

In einer Formularvorlage für verwalteten Code, die mithilfe des objektmodells erstellt wurde, das von den Mitgliedern der [Microsoft.Office. InfoPath-Namespace:](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Sie können das Schlüsselwort this **(C#)** oder **Me** (Visual Basic) im Formularcode verwenden, um direkt auf die Member der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zu zugreifen (ohne eine Objektvariable zu benötigen, die einen Verweis auf die [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) erstellt). 
  
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

Eine wichtige Eigenschaft der **XmlForm**-Klasse hinsichtlich Formulardaten ist die **MainDataSource**-Eigenschaft. Diese Eigenschaft gibt einen Verweis auf ein [DataSource-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) zurück, das die zugrunde liegenden XML-Daten des aktuellen Formulars darstellt, das auch als haupt- oder primäre Datenquelle des Formulars bezeichnet wird. Die **DataSource-Klasse** bietet die [CreateNavigator-Methode,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) mit der ein [XPathNavigator-Objekt](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) erstellt wird, das am Stamm des dem Formular zugrunde liegenden XML-Dokuments positioniert ist. Die Eigenschaften und Methoden der **XPathNavigator**-Klasse können dann verwendet werden, um in den zugrunde liegenden XML-Daten des Formulars zu navigieren und sie zu bearbeiten. 
  
Im folgenden Beispiel wird die **MainDataSource**-Eigenschaft der **XmlForm**-Klasse zum Erstellen eines **XPathNavigator**-Objekts verwendet, das im Stammknoten der Hauptdatenquelle des Formulars positioniert ist. Die **OuterXml-Eigenschaft** der **XPathNavigator-Klasse** wird dann verwendet, um den gesamten Inhalt des einem Formular zugrunde liegenden XML-Dokuments zurück und anzuzeigen. 
  
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
  
Weitere Informationen zur **XPathNavigator-Klasse** in der Geschäftslogik einer InfoPath-Formularvorlage finden Sie unter Arbeiten mit den [Klassen XPathNavigator und XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Zugreifen auf Daten über die Formularvorlagendatei eines Formulars

Auf Informationen zu einem Formular zugeordnete Formularvorlage, einschließlich der Formulardefinitionsdatei (XSF) und der enthaltenen XML-Daten kann auch mithilfe der **XmlForm**-Klasse zugegriffen werden. Auf diese Informationen wird mithilfe der [Template-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) zugegriffen, die einen Verweis auf ein [FormTemplate-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) zurückgibt, das die dem aktuellen Formular zugeordnete Formularvorlage darstellt. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten an, die über die **Template-Klasse** verfügbar sind, z. B. den Speicherort des URI (Uniform Resource Identifier) (mithilfe der [Uri-Eigenschaft),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) den Cachebezeichner (mithilfe der [CacheId-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) und dessen Versionsnummer (mithilfe der [Version-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) Im nächsten Meldungsfeld wird die [Manifest-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) der **Template-Klasse** verwendet, um ein **XPathNavigator-Objekt** zu erstellen, das zum Anzeigen der Quell-XML der Formulardefinitionsdatei (XSF) verwendet wird. 
  
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


