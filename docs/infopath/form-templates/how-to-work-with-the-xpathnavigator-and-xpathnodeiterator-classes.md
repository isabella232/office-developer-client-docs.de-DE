---
title: Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- xpathnodeiterator class [infopath 2007],XPathNavigator class [InfoPath 2007],form XML data [InfoPath 2007], accessing,XML DOM [InfoPath 2007],converting MSXML5 script [InfoPath 2007],MSXML5 script [InfoPath 2007], converting
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Um auf die XML-Daten in Formularvorlagendatenquellen zu zugreifen und diese zu bearbeiten, werden viele Elemente des von Microsoft bereitgestellten Objektmodells für verwalteten Code verwendet. Office. InfoPath-Namespace erstellt oder kann eine Instanz der XPathNavigator-Klasse des System.Xml. XPath-Namespace. Wenn Sie Zugriff auf einXPathNavigator-Objekt erhalten haben, das von einem InfoPath-Objektmodellmember zurückgegeben wird, können Sie die Eigenschaften und Methoden der XPathNavigator-Klasse verwenden, um mit den Daten zu arbeiten.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303549"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator

Um auf die XML-Daten in Formularvorlagendatenquellen zu zugreifen und diese zu bearbeiten, werden viele Elemente des objektmodells für verwalteten Code von [Microsoft.Office. InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) erstellt oder kann eine Instanz der **XPathNavigator-Klasse** des **System.Xml. XPath-Namespace.** Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt erhalten haben, das von einem InfoPath-Objektmodellmember zurückgegeben wird, können Sie die Eigenschaften und Methoden der **XPathNavigator**-Klasse verwenden, um mit den Daten zu arbeiten. 
  
Das am häufigsten verwendete Mitglied der **Microsoft.Office. Der** InfoPath-Namespace, der die **XPathNavigator-Klasse** verwendet, ist die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) der [DataSource-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) mit der Sie mit den gespeicherten Daten arbeiten können, die durch ein **DataSource-Objekt** dargestellt werden. Von der **CreateNavigator**-Methode wird ein **XPathNavigator**-Objekt am Stamm der Datenquelle erstellt, die vom **DataSource**-Objekt dargestellt wird. 
  
> [!TIP]
> Wenn Sie mit der Verwendung von MSXML5 aus Skript zum Arbeiten mit Daten in Microsoft InfoPath 2003 vertraut sind, können Sie sich die **CreateNavigator**-Methode als Ersatz für die **DOM**-Eigenschaft von **DataObject** vorstellen. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Verwenden der "XPathNavigator"-Klasse für den Zugriff auf die Hauptdatenquelle des Formulars

Um auf die Hauptdatenquelle des Formulars zu zugreifen, rufen Sie die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) direkt über das Schlüsselwort **C#** oder **Me** (Visual Basic) auf. Im folgenden Codebeispiel wird ein **XPathNavigator**-Objekt am Stamm der Hauptdatenquelle mithilfe der **CreateNavigator**-Methode erstellt, und dann wird die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen. 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> Das Aufrufen der [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) direkt aus dem **This-** oder **Me-Schlüsselwort** entspricht dem Aufrufen der [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) mithilfe der [MainDataSource-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( ) oder durch Übergeben einer leeren Zeichenfolge an die  `this.MainDataSource.CreateNavigator()` [DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()` ). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Auswählen und Festlegen der XML-Knoten für Felder in der Hauptdatenquelle
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Verwenden Sie zum Auswählen des einzelnen XML-Knotens für ein Feld in einer Datenquelle die **SelectSingleNode(String,IXmlNamespaceResolver)-Methode** der **XPathNavigator-Klasse.** Wenn Sie mit einer Reihe wiederholter Felder oder wiederholter Gruppen arbeiten möchten, verwenden Sie die **Select(String,IXmlNamespaceResolver)-Methode** der **XPathNavigator-Klasse.** Diese Methode gibt ein **XPathNodeIterator-Objekt zurück,** das eine Auflistung von Knoten darstellt. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Auswählen und Festlegen des Werts eines einzelnen Knotens

Die überladene **SelectSingleNode-Methode,** die Sie verwenden müssen, verfügt über einen  _xpath-Parameter,_ der einen XPath-Ausdruck als Zeichenfolge verwendet, und einen  _Resolverparameter,_ der ein **XmlNamespaceManager-Objekt** zum Auflösen von Namespacepräfixen verwendet. Um einen einzelnen Knoten in der Hauptdatenquelle des Formulars auszuwählen, übergeben Sie einen XPath-Ausdruck, der das Feld oder die Gruppe angibt, die Sie für den  _xpath-Parameter_ auswählen möchten, zusammen mit dem **XmlNamespaceManager-Objekt,** das von der [NamespaceManager-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) des **XmlForm-Objekts zurückgegeben** wird. Das zurückgegebene **XmlNamespaceManager**-Objekt wird mit allen Namespates, die in der Formulardefinitionsdatei (XSF) der Formularvorlage definiert sind, zum Ladezeitpunkt initialisiert. 
  
> [!TIP]
> Die einfachste Möglichkeit zum Erstellen eines XPath-Ausdrucks zum Auswählen eines Knotens in der Datenquelle des Formulars ist das Klicken mit der rechten Maustaste im Aufgabenbereich **Felder** auf das Feld oder die Gruppe und anschließende Klicken auf **XPath kopieren**. Fügen Sie zum Erstellen und Testen manuell bearbeiteter XPath-Ausdrücke für den Zugriff auf Knoten in einem komplexen oder überaus geschachtelten XML-Schema dem Formular ein Steuerelement vom Typ **Ausdrucksfeld** hinzu. Geben Sie dann den XPath-Ausdruck für das Steuerelement an, und zeigen Sie anschließend eine Vorschau des Formulars an, um die Ergebnisse anzuzeigen. 
  
Im folgenden Beispiel wird die **SelectSingleNode-Methode** verwendet, um den einzelnen Knoten für das Feld  `EmailAlias` auszuwählen. Anschließend wird die **SetValue-Methode** der **XPathNavigator-Klasse** und die [UserName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) der [User-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) verwendet, um den Wert des Felds auf den Alias des aktuellen Benutzers zu setzen. 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

Informationen zum Erstellen von XPath-Ausdrücken finden Sie in der XPath-Referenz auf MSDN und in der [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Festlegen des Werts eines Knotens mit dem Attribut "xsi:nil"

Bei bestimmten Datentypen wird beim Versuch, den Wert eines leeren Felds programmgesteuert festzulegen, der Fehler "Nicht datentypbezogene Fehler bei der Schemaüberprüfung" angezeigt. In der Regel ist die Ursache dieses Fehlers, dass für das Element das [xsi:nil-Attribut](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) auf **true festgelegt ist.** Wenn Sie das zugrunde liegende XML-Element des leeren Felds im Formular untersuchen, können Sie diese Einstellung erkennen. Im XML-Fragment des folgenden leeren "Date"-Felds ist z. B. das **xsi:nil**-Attribute auf **true** festgelegt.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Wenn das **xsi:nil-Attribut** auf **true** festgelegt ist, gibt es an, dass das Element vorhanden ist, aber keinen Wert hat, oder anders ausgedrückt, null ist. Wenn Sie versuchen, den Wert eines solchen Knotens programmgesteuert zu setzen, zeigt InfoPath die Meldung "Schemaüberprüfung gefundene Nicht-Datentypfehler" an, da das Element derzeit als null gekennzeichnet ist. InfoPath legt das **xsi:nil**-Attribut für null-Felder der folgenden Datentypen auf **true** fest: 
  
- **Ganze Zahl (ganze Zahl)**
    
- **Decimal (double)**
    
- **Datum (Datum)**
    
- **Zeit (Zeit)**
    
- **Datum und Uhrzeit (dateTime)**
    
Zum Vermeiden dieses Fehlers muss Ihr Code prüfen, ob das **xsi:nil**-Attribut vorhanden ist, und falls ja, es entfernen, bevor der Wert des Knotens festgelegt wird. Die folgende Unterroutine verwendet ein **XpathNavigator**-Objekt am Knoten, den Sie festlegen möchten, sucht nach dem **nil**-Attribut und löscht es, sofern vorhanden. 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "https://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "https://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

Sie können diese Unterroutine aufrufen, bevor Sie versuchen, ein Feld eines Datentyps festzulegen, das ggf. das **xsi:nil**-Attribut aufweist (siehe das folgende Beispiel, das ein "Date"-Feld festlegt). 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> Obwohl die Implementierung des **XPathNavigator-Objekts** in InfoPath die **SetTypedValue-Methode** verfügbar macht, die zum Festlegen eines Knotens mithilfe eines bestimmten Typs verwendet wird, implementiert InfoPath diese Methode nicht. Sie müssen stattdessen die **SetValue**-Methode verwenden und einen Zeichenfolgenwert im ordnungsgemäßen Format für den Datentyp des Knotens übergeben. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Auswählen und Festlegen eines Satzes wiederholter Knoten

Verwenden Sie die **Select-Methode** der **XPathNavigator-Klasse,** um einen Satz wiederholter Felder oder Gruppen anzugeben, die einer unbestimmten Zahl entsprechen. Diese Methode gibt ein XPathNodeIterator-Objekt zurück, mit dem Sie die angegebene Auflistung von Knoten durch iterieren können. 
  
Im folgenden Beispiel wird davon ausgegangen, dass Ihre Formularvorlage ein Aufzählungszeichen oder ein ähnliches wiederholtes Steuerelement enthält, das an ein wiederholtes Element namens gebunden  `field1` ist. Der XPath des Felds wird an die **Select-Methode** übergeben, und der zurückgegebene **XPathNodeIterator** wird der Variablen  `nodes` zugewiesen. Sie verwenden die MoveNext-Methode, um die Auflistung von Knoten zu durch iterieren, und die Current-Eigenschaft gibt ein **XPathNavigator-Objekt** zurück, das auf dem aktuellen Knoten positioniert ist. Verwenden Sie schließlich die **Value-Eigenschaft,** um den Wert jedes wiederholten Felds abzurufen und zu anzeigen. 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

Das vorherige Beispiel funktioniert mit Zeichenfolgenwerten im angegebenen wiederholten Feld. Wenn das Feld jedoch numerische Werte enthält, können Sie ähnlichen Code verwenden, um die Werte im Feld für Berechnungen, z. B. der Summe der Werte oder ihres Durchschnitts, zu durchlaufen.
  
Anstatt die **Value**-Eigenschaft zum Abrufen des Werts jeder Instanz des wiederholten Felds zu verwenden, können Sie auch mithilfe der **SetValue**-Methode die Felder durchlaufen und ihre Werte festlegen (siehe das folgende Beispiel). 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Verwenden der "XPathNavigator"-Klasse für den Zugriff auf eine externe Datenquelle
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Um auf eine externe Datenquelle zu zugreifen, die dem Formular zugeordnet ist, übergeben Sie den Namen der Datenquelle an die [DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) der [XmlForm-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Klicken Sie zum Herstellen einer Verbindung mit einer neuen externen Datenquelle oder zum Anzeigen einer Liste der Namen der vorhandenen Verbindungen mit externen Datenquellen im Menüband auf der Registerkarte **Daten** auf **Datenverbindungen**. 
  
Im folgenden Codebeispiel wird gezeigt, wie ein **XPathNavigator**-Objekt am Stamm einer externen Datenquelle mit dem Namen "CityList" mithilfe der **CreateNavigator**-Methode erstellt wird und dann die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet wird, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen. Dieses Codebeispiel geht davon aus, dass Sie eine Datenverbindung mit einer Liste von Ortsnamen erstellt haben, die in einer externen Datenquelle gespeichert sind, z. B. in einem XML-Dokument oder einer SharePoint-Liste, und die Datenverbindung "CityList" genannt haben. 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt am Stamm der externen Datenquelle erhalten haben, können Sie mithilfe von Members der **XPathNavigator**-Klasse wie den Methoden **SelectSingleNode** und **SetValue** mit den enthaltenen Daten arbeiten. 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>InfoPath-Objektmodellmember, von denen die Klassen "XPathNavigator" und "XPathNodeIterator" verwendet werden
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Die folgende Tabelle enthält eine Übersicht aller Member des **Microsoft.Office.InfoPath**-Namespace, von denen die **XPathNavigator**-Klasse verwendet wird, um auf XML-Daten zuzugreifen, sie zu bearbeiten oder zu senden. 
  
|**Übergeordnete Klasse**|**Element**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[BuildSqlFromXmlNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Source-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Context-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||[GetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||[SetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Hinzufügen von](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) Methoden  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[Xml-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Signatur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[SignatureBlockXmlNode-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[SignatureContainer-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[SelectNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||[SelectText-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||[GenerateDataSetDiffGram-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[OldParent-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||[Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[MainDataSource-Eigenschaft,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) die ein **DataSource-Objekt** zurückgibt, das wiederum die **CreateNavigator-Methode** zum Erstellen eines **XPathNavigator-Objekts** am Stamm des dem Formular zugrunde liegenden XML-Dokuments (Hauptdatenquelle) zur Verfügung stellt.  <br/> |
||[MergeForm-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[NewFromFormTemplate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
Neben den InfoPath-Objektmodellmembern, die ein **XPathNavigator**-Objekt zurückgeben oder annehmen, geben die folgenden Methoden eine Instanz der **XPathNodeIterator**-Klasse des **System.Xml.XPath**-Namespace zum Durchlaufen der XML-Knoten von Elementen zurück, die in einer Ansicht angegeben oder ausgewählt werden. 
  
|**Übergeordnete Klasse**|**Element**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Verwenden der Klassen "XPathNavigator" und "XPathNodeIterator" für in einer Ansicht ausgewählte Daten
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Im folgenden Beispiel werden Member der Klassen **XPathNavigator** und **XPathNodeIterator** für Formulardaten in der folgenden Reihenfolge verwendet: 
  
1. Die **CreateNavigator-Methode** der **DataSource-Klasse** wird zum Erstellen einer **XPathNavigator-Objektvariablen** namens repeatingTableRow1 verwendet, die standardmäßig am Stamm des zugrunde liegenden XML-Dokuments des Formulars (der Hauptdatenquelle) positioniert ist.
    
2. Die **SelectSingleNode-Methode** der **XPathNavigator-Klasse** wird verwendet, um die Position des **XPathNavigator-Objekts** in die erste Zeile eines **Steuerelements** für wiederholte Tabelle zu verschieben, das an Group2 in der Datenquelle gebunden ist. 
    
3. Die repeatingTableRow1-Objektvariable wird an die **SelectNodes**-Methode der **View**-Klasse übergeben, um die Knoten in dieser Zeile auszuwählen. 
    
4. Eine **XPathNodeIterator-Objektvariable** namens selectedNodes wird deklariert, und die **GetSelectedNodes-Methode** der **View-Klasse** wird verwendet, um das **XPathNodeIterator-Objekt** mit den ausgewählten Knoten zu füllen. 
    
5. Mit **der Count-Eigenschaft** der **XPathNodeIterator-Klasse** wird die Anzahl der Knoten angezeigt, die in der selectedNodes-Objektvariablen enthalten sind. 
    
6. Eine For/Each-Schleife dient zum Durchlaufen der Knoten in der selectedNodes-Objektvariablen und zum Anzeigen von Informationen zu den einzelnen Knoten mithilfe der Eigenschaften **Name**, **InnerXml** und **Value** der **XPathNavigator**-Klasse. 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

Weitere Informationen zum Arbeiten mit XML-Daten aus InfoPath-Formularvorlagen finden Sie unter Arbeiten mit XML-Daten mithilfe der XPathNavigator-Klasse in InfoPath 2007-Formularvorlagen.
  

