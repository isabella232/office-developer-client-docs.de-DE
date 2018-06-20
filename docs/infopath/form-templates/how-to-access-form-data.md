---
title: Access-Formulardaten
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- forms-Formulardaten [Infopath 2007], [InfoPath 2007], zugreifen auf Eigenschaften,-Formularvorlagen [InfoPath 2007], zugreifen auf Eigenschaften, und Öffnen von Formularen [InfoPath 2007], Drucken von Formularen [InfoPath 2007], Formularen [InfoPath 2007], drucken, Schließen von Formularen [InfoPath 2007] Zugreifen auf Formulardaten, Formularen [InfoPath 2007], zugreifen auf Datenquelle, Formularen [InfoPath 2007], schließenden, Formularen [InfoPath 2007], öffnen, Drucken [InfoPath 2007], Formulare, Formularen [InfoPath 2007], Erstellen von InfoPath 2007
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es oft notwendig, den programmgesteuerten Zugriff auf Informationen zu dem Formular zugrunde liegenden XML-Dokument, Zugriff auf die Daten, die das XML-Dokument enthält oder Aktionen auf dem XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und Bearbeitung von einem Formular zugrunde liegenden XML-Dokument mithilfe der XmlForm-Klasse im Zusammenhang mit der XmlFormCollection-Klasse.
ms.openlocfilehash: c39862fd404575fe95bc1986ce7ab7d9689acfb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790772"
---
# <a name="access-form-data"></a>Access-Formulardaten

Wenn Sie die Funktionalität eines InfoPath-Formulars erweitern möchten, ist es oft notwendig, den programmgesteuerten Zugriff auf Informationen zu dem Formular zugrunde liegenden XML-Dokument, Zugriff auf die Daten, die das XML-Dokument enthält oder Aktionen auf dem XML-Dokument auszuführen. Das InfoPath-Objektmodell unterstützt den Zugriff auf und Bearbeitung von einem Formular zugrunde liegenden XML-Dokument mithilfe der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse im Zusammenhang mit der [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) -Klasse. 
  
[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse ist eine der nützlichsten Typen im InfoPath-Objektmodell, da es eine Vielzahl von Eigenschaften bietet und Methoden, die nicht nur mit einem Formular zugrunde liegenden XML interagieren-Dokument, sondern auch ausführen viele der Aktionen, die in verfügbar sind die InfoPath-Benutzeroberfläche. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Übersicht über die XmlFormCollection-Klasse

Die [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler verwenden können zum Verwalten der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekte, die die Auflistung enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) -Methode  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular.  <br/> |
|[Neu (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) -Methode (Überladung 1)  <br/> |Erstellt basierend auf dem angegebenen Formular ein neues Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[-Objekt zu](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode  <br/> |Erstellt basierend auf der angegebenen Formularvorlage ein neues Formular.  <br/> |
|[NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Überladung 1)  <br/> |Erstellt basierend auf der angegebenen Formularvorlage und XML-Daten ein neues Formular.  <br/> |
|[NewFromFormTemplate (String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Überladung 2)  <br/> |Erstellt ein neues Formular basierend auf der angegebenen Formularvorlage mit Daten, die durch ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt angegeben.  <br/> |
|[NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode (Überladung 3)  <br/> |Erstellt ein neues Formular basierend auf der angegebenen Formularvorlage mit Daten, die durch ein **XPathNavigator** -Objekt mithilfe des angegebenen öffnungsmodusverhaltens angegeben.  <br/> |
|[Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) -Methode  <br/> |Öffnet das angegebene Formular.  <br/> |
|[Open (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) -Methode (Überladung 1)  <br/> |Öffnet das angegebene Formular mithilfe des angegebenen Öffnungsmodusverhaltens.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **XmlForm** -Objekte in der Auflistung ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene **XmlForm** -Objekt aus der Auflistung anhand des Indexwertes ab.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Übersicht über die XmlForm-Klasse

[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit und Ausführen von Aktionen für das einem Formular zugrunde liegenden XML-Dokument verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)-Methode  <br/> |Schließt das Formular.  <br/> |
|[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) -Methode  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTasks** -Auflistung für das aktuelle Formular ab.  <br/> |
|[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) -Methode  <br/> |Ruft einen Verweis auf die **Microsoft.Office.Core.WorkflowTemplates** -Auflistung für das aktuelle Formular ab.  <br/> |
|[MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode  <br/> |Führt das aktuelle Formular mit dem über den Pfad oder URL angegebenen Formular zusammen.  <br/> |
|[MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode (Überladung 1)  <br/> |Führt das aktuelle Formular mit dem angegebenen Knoten zurückgegebene **XPathNavigator** Zielformular an die Methode übergeben.  <br/> |
|[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) -Methode  <br/> |Stellt einen benutzerdefinierten Wert für die Hostanwendung oder ASPX-Seite (Active Server Page Extension) bereit.  <br/> |
|[Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) -Methode  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird.  <br/> |
|[Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) -Methode (Überladung 1)  <br/> |Druckt den Formularinhalt so, wie er in der aktiven Ansicht des Formulars gerendert wird, indem das Dialogfeld **Drucken** angezeigt.  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)-Methode  <br/> |Speichert das Formular unter dem ihr zurzeit zugeordneten URL (Uniform Resource Locator).  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)-Methode  <br/> |Speichert das Formular unter dem angegebenen URL (Uniform Resource Locator).  <br/> |
|[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) -Methode  <br/> |Legt den Standarddateinamen für das Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) -Methode  <br/> |Legt den Standardpfad für das Formular mithilfe **des Dialogfeldes** speichern.  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) -Methode  <br/> |Sendet das Formular mithilfe des in der Formularvorlage definierten Sendevorgangs.  <br/> |
|[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft  <br/> |Ruft ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt, das die aktuelle Ansicht des Formulars darstellt.  <br/> |
|[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) -Eigenschaft  <br/> |Ruft ein [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) -Objekt, das dem Formular zugeordnet.  <br/> |
|[DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) (Eigenschaft)  <br/> |Ruft das dem Formular zugeordnete [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) -Objekt.  <br/> |
|[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob die Daten in einem Formular seit dem letzten Speichern geändert wurden.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) , das einem Formular zugeordnet ist.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) -Eigenschaft  <br/> |Ruft ein [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) für den Zugriff auf die Funktionen und globalen Variablen, die in einem Formular zugrunde primären Formularcodedatei mithilfe von [System.Reflection](https://msdn.microsoft.com/en-us/library/system.reflection(v=vs.110).aspx)enthalten sind.  <br/> |
|[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf eine Eigenschaftensammlung vom Typ [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) , die von browserfähigen Formularen zum Beibehalten von Statusinformationen in allen Sitzungen auf dem Server verwenden können.  <br/> |
|[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) -Eigenschaft  <br/> |Ruft ein [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) , die in einer gehosteten Instanz von InfoPath ausgeführten Code zum Zugreifen auf das Objektmodell der hostanwendung verwenden können.  <br/> |
|[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) -Eigenschaft  <br/> |Ruft ab, ob InfoPath in einer anderen Anwendung als Steuerelement gehostet wird.  <br/> |
|[HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) -Eigenschaft  <br/> |Ruft den Namen der Anwendung ab, mit der InfoPath als Steuerelement gehostet wird.   <br/> |
|[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft  <br/> |Ruft ein [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt, das die Hauptdatenquelle des Formulars darstellt.  <br/> |
|[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) -Objekt, das zum Auflösen, hinzufügen oder Entfernen der im Formular verwendeten Namespaces verwendet werden kann.  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular neu ist.  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) -Objekt, das dem Formular zugeordnet.  <br/> |
|[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) -Objekt, das die Datenverbindung darstellt, die dem Formular zugeordnet ist.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob eine Formularvorlage schreibgeschützt oder gesperrt ist.  <br/> |
|[Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular zuletzt mithilfe eines AutoWiederherstellen-Speichervorgangs gespeichert wurde.  <br/> |
|[Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) -Eigenschaft  <br/> |Ruft einen Wert ab, der angibt, ob ein Formular mithilfe digitaler Signaturen digital signiert wurde.  <br/> |
|[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Auflistung, die einem Formular zugeordnet ist.  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) , die einer Formularvorlage zugeordnet ist.  <br/> |
|[Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf das [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) -Objekt, das Manifest (XSF) der Formularvorlage, die dem Formular zugeordneten darstellt.  <br/> |
|[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)-Eigenschaft  <br/> |Ruft den URI (Uniform Resource Identifier) eines Formulars ab.  <br/> |
|[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) -Eigenschaft  <br/> |Ruft den aktuellen Benutzer des Rollennamens im Formular ab oder legt diesen fest.  <br/> |
|[ViewInfos (](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) Eigenschaft)  <br/> |Ruft einen Verweis auf das der Formularvorlage zugeordnete [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Objekt ab.  <br/> |
|[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) -Eigenschaft  <br/> |Ruft den Wert des **XML: lang** -Attributs im zugrunde liegenden XML-Dokument des Formulars ab.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Verwenden der XmlFormCollection-Klasse

Der Zugriff auf die **XmlFormCollection** -Klasse erfolgt über die [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse. In einer verwalteten Code-Formularvorlage mit durch die Member des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell erstellt können das **diese** (c#) oder Schlüsselwort **Me** (Visual Basic) im Formularcode Sie die **Anwendung zugreifen **-Klasse und ihre Member. 
  
Das folgende Beispiel verwendet die **XmlForms** -Eigenschaft des **Application** -Klasse erstellen Sie eine Objektvariable, die mit dem Namen MyForms, die das **XDocumentsCollection** -Objekt der derzeit ausgeführten Instanz von InfoPath verweist. Diese Variable wird dann verwendet, um die Anzahl der Formulare anzuzeigen, die geöffnet sind. 
  
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

Die Variable MyForms kann dann auch zum Erstellen neuer Formulare (mithilfe einer der Methoden **New** oder **NewFromTemplate** ) oder zum Öffnen vorhandener Formulare (mithilfe einer der **Open** -Methoden) verwendet werden. 
  
## <a name="using-the-xmlform-class"></a>Verwenden der XmlForm-Klasse

In einer verwalteten Code-Formularvorlage mit durch die Member des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell erstellt können das **diese** (c#) oder Schlüsselwort **Me** (Visual Basic) im Formularcode Sie den Zugriff auf die Member der [ XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Klasse direkt (ohne dass eine Objektvariable, die einen Verweis auf das [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse stellt her). 
  
### <a name="accessing-a-forms-property-values"></a>Zugreifen auf die Eigenschaftenwerte eines Formulars

Das folgende Beispiel verwendet das **this** oder **Me** -Schlüsselwort zum Zugriff auf die Eigenschaften **New**, **ReadOnly**, **Signed**und **Uri** der **XmlForm** -Klasse und Anzeigen der Werte für das aktuelle Formular in einem Meldungsfeld zurückgegeben . 
  
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

Eine wichtige Eigenschaft der **XmlForm** -Klasse im Hinblick auf die Formulardaten ist die **MainDataSource** -Eigenschaft. Diese Eigenschaft gibt einen Verweis auf ein [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt, das die zugrunde liegenden XML-Daten des aktuellen Formulars darstellt, das auch als Haupt- oder primären Datenquelle des Formulars bezeichnet wird. Die **DataSource** -Klasse stellt die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode, die ein [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Objekt befindet sich im Stamm des dem Formular zugrunde liegenden XML-Dokument erstellt wird. Die Eigenschaften und Methoden der **XPathNavigator** -Klasse können Sie dann zum Navigieren und bearbeiten dem Formular zugrunde liegenden XML-Daten verwendet werden. 
  
Im folgende Beispiel wird die **MainDataSource** -Eigenschaft der **XmlForm** -Klasse zum Erstellen eines **XPathNavigator** -Objekts am Stamm der Hauptdatenquelle des Formulars verwendet. Die **OuterXml** -Eigenschaft der **XPathNavigator** -Klasse wird zum Zurückgeben und Anzeigen der Inhalt des einem Formular zugrunde liegenden XML-Dokument verwendet. 
  
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
> Da InfoPath die **MainDataSource** -Eigenschaft als Standardeigenschaft des **XmlForm** -Objekts zugegriffen, wenn das **this** oder **Me** Schlüsselwörter mit behandelt, können Sie es aus die Codezeile, die zum Erstellen der **"XPathNavigator"** ausschließen. -Objekt. 
  
Weitere Informationen zu der **XPathNavigator** -Klasse in einer InfoPath-Formularvorlage Geschäftslogik finden Sie unter [Arbeiten mit dem XPathNavigator und XPathNodeIterator-Klassen](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Zugreifen auf Daten über die Formularvorlagendatei eines Formulars

Informationen zu der Formularvorlage zugeordneten eines Formulars, einschließlich der Formulardefinitionsdatei (XSF) und den XML-Quelldaten, die er enthält, kann auch unter Verwendung der **XmlForm** -Klasse zugegriffen werden. Diese Informationen erfolgt mit der [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) -Eigenschaft, die einen Verweis auf ein [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) -Objekt zurückgibt, die dem aktuellen Formular zugeordnete Formularvorlage darstellt. 
  
Im folgenden Beispiel zeigt das erste Meldungsfeld einige der Daten, die über die **Vorlage** -Klasse, z. B. den Uniform Resource Identifier (URI)-Speicherort (mithilfe der [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) -Eigenschaft), verfügbar sind der Cachebezeichner (mithilfe der [CacheId ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx)-Eigenschaft) und die Versionsnummer (mithilfe der [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) -Eigenschaft). Das nächste Meldungsfeld verwendet die Eigenschaft [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) der **Vorlage** -Klasse ein **XPathNavigator** -Objekt zu erstellen, die zum Anzeigen der XML-Quelldaten der Formulardefinitionsdatei (XSF) verwendet wird. 
  
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


