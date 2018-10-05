---
title: Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- XPathNodeIterator-Klasse [Infopath 2007], XPathNavigator-Klasse [InfoPath 2007], XML-Formulardaten [InfoPath 2007], den Zugriff auf XML-DOM [InfoPath 2007], Konvertieren von MSXML5-Skript [InfoPath 2007], MSXML5-Skript [InfoPath 2007], konvertieren
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Zugriff und zum Bearbeiten der XML-Datenteils im Formular Vorlage Datenquellen, viele Mitglieder der vom Microsoft.Office.InfoPath-Namespace bereitgestellten Objektmodell für verwalteten Code erstellen oder eine Instanz der XPathNavigator-Klasse von der Auswertungsmodul übergeben werden kann Namespace. Nachdem Sie den Zugriff auf ein XPathNavigator-Objekt zurückgegeben, die durch ein InfoPath-Objektmodellmember haben, können Sie die Eigenschaften und Methoden der XPathNavigator-Klasse zum Arbeiten mit den Daten verwenden.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393040"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"

Zugriff und zum Bearbeiten der XML-Datenteils im Formular Vorlage Datenquellen, viele Mitglieder der vom [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellten Objektmodell für verwalteten Code erstellen oder eine Instanz der **XPathNavigator** -Klasse übergeben werden kann die **Auswertungsmodul** -Namespace. Nachdem Sie den Zugriff auf ein **XPathNavigator** -Objekt zurückgegeben, die durch ein InfoPath-Objektmodellmember haben, können Sie die Eigenschaften und Methoden der **XPathNavigator** -Klasse zum Arbeiten mit den Daten verwenden. 
  
Der am häufigsten verwendete Member des **Microsoft.Office.InfoPath** -Namespace, der die **XPathNavigator** -Klasse verwendet wird, die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse, die Sie mit den gespeicherten Daten arbeiten können durch ein **DataSource** -Objekt dargestellt. Die **CreateNavigator** -Methode erstellt ein am Stamm der durch das **DataSource** -Objekt dargestellte Datenquelle positioniertes **XPathNavigator** -Objekt. 
  
> [!TIP]
> Wenn Sie mit der Verwendung von MSXML5 aus Skript zum Arbeiten mit Daten in Microsoft InfoPath 2003 vertraut sind, können Sie sich die **CreateNavigator**-Methode als Ersatz für die **DOM**-Eigenschaft von **DataObject** vorstellen. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Verwenden der "XPathNavigator"-Klasse für den Zugriff auf die Hauptdatenquelle des Formulars

Rufen Sie den Zugriff auf die Hauptdatenquelle des Formulars die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode direkt über das **dieses** (c#) oder Schlüsselwort **Me** (Visual Basic). Im folgende Beispiel ein **XPathNavigator** -Objekts am Stamm der Hauptdatenquelle mithilfe der **CreateNavigator** -Methode erstellt, und klicken Sie dann die **OuterXml** -Eigenschaft der **XPathNavigator** -Klasse verwendet, um die XML-Daten anzeigen in einem Meldungsfeld zurückgegeben. 
  
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
> Aufrufen von die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode direkt über das **this** oder **Me** -Schlüsselwort ist gleichbedeutend mit dem [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode mit der [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft ( `this.MainDataSource.CreateNavigator()`) oder indem Sie eine leere Zeichenfolge an die [ DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse ( `this.DataSources[""].CreateNavigator()`). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Auswählen und Festlegen der XML-Knoten für Felder in der Hauptdatenquelle
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Um die einzelnen XML-Knoten für ein Feld in einer Datenquelle auswählen möchten, verwenden Sie die **SelectSingleNode(String,IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse. Wenn Sie mit einem Satz von wiederholte Felder oder wiederholte Gruppen arbeiten möchten, verwenden Sie die **Select(String,IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse. Diese Methode gibt ein **XPathNodeIterator** -Objekt, das eine Auflistung von Knoten darstellt. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Auswählen und Festlegen des Werts eines einzelnen Knotens

Die überladene **SelectSingleNode** -Methode, die Sie verwenden müssen verfügt über einen _Xpath_ -Parameter, der einen XPath-Ausdruck als Zeichenfolge annimmt, und einen _Auflösung_ -Parameter, der ein **XmlNamespaceManager** -Objekt für die Beilegung von Namespace akzeptiert Präfixe. Um einen einzelnen Knoten in der Hauptdatenquelle des Formulars auszuwählen, übergeben Sie einen XPath-Ausdruck, der angibt, das Feld oder Gruppe, die Sie für den _Xpath_ -Parameter zusammen mit dem **XmlNamespaceManager** -Objekt auswählen möchten, die von der [zurückgegeben wird NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) -Eigenschaft der **XmlForm** -Objekt. Das zurückgegebene **XmlNamespaceManager** -Objekt wird zur Ladezeit mit allen Namespaces initialisiert, die von der Formulardefinitionsdatei (XSF) der Formularvorlage definiert sind. 
  
> [!TIP]
> Die einfachste Möglichkeit zum Erstellen eines XPath-Ausdrucks zum Auswählen eines Knotens in der Datenquelle des Formulars ist das Klicken mit der rechten Maustaste im Aufgabenbereich **Felder** auf das Feld oder die Gruppe und anschließende Klicken auf **XPath kopieren**. Fügen Sie zum Erstellen und Testen manuell bearbeiteter XPath-Ausdrücke für den Zugriff auf Knoten in einem komplexen oder überaus geschachtelten XML-Schema dem Formular ein Steuerelement vom Typ **Ausdrucksfeld** hinzu. Geben Sie dann den XPath-Ausdruck für das Steuerelement an, und zeigen Sie anschließend eine Vorschau des Formulars an, um die Ergebnisse anzuzeigen. 
  
Das folgende Beispiel verwendet die **SelectSingleNode** -Methode für den einzelnen Knoten aus der `EmailAlias` dar. Anschließend werden die **SetValue** -Methode der **XPathNavigator** -Klasse und die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse für den Wert des Felds festzulegen, den Alias des aktuellen Benutzers verwendet. 
  
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

Informationen zum Erstellen von XPath-Ausdrücken finden Sie unter der XPath-Referenz auf MSDN und die [Empfehlung für XML Path Language (XPath) Version 1.0 W3C](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Festlegen des Werts eines Knotens mit dem Attribut "xsi:nil"

Für bestimmte Datentypen wird versucht, den Wert eines leeren Feldes programmgesteuert festlegen der Fehler "schemavalidierung wurden nicht vom Datentyp Fehler gefunden." In der Regel ist die Ursache für diesen Fehler an, dass das Element das [xsi: nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) -Attribut auf **true**festgelegt wurde. Wenn Sie das zugrunde liegende XML-Element für das leere Feld in der Form untersuchen, können Sie diese Einstellung finden Sie unter. Das XML-Fragment für die folgenden leeren Datumsfeld verfügt beispielsweise über das **xsi: nil** -Attribut auf **true**festgelegt.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Wenn das **xsi: nil** -Attribut auf **true**festgelegt ist, bedeutet dies, dass das Element vorhanden ist, jedoch wird kein Wert oder mit anderen Worten, null ist. Wenn Sie versuchen, den Wert eines solchen Knotens programmgesteuert festlegen, zeigt InfoPath die Meldung "schemavalidierung found nicht-Datentyp-Fehler" an, da das Element derzeit als null gekennzeichnet ist. InfoPath legt das **xsi: nil** -Attribut auf **true** für null-Felder der folgenden Datentypen: 
  
- **Ganze Zahl (Integer)**
    
- **Dezimalzahl (Double)**
    
- **Datum (Date)**
    
- **Uhrzeit)**
    
- **Datum und Uhrzeit (DateTime)**
    
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
> Obwohl die Implementierung der **XPathNavigator** -Objekt in InfoPath die **SetTypedValue** -Methode verfügbar macht – die wird verwendet, um einen Knoten mit einem Wert eines bestimmten Typs festlegen – InfoPath diese Methode nicht implementiert. Sie müssen stattdessen die **SetValue** -Methode, und übergeben Sie einen String-Wert, der das richtige Format für den Datentyp des Knotens. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Auswählen und Festlegen eines Satzes wiederholter Knoten

Verwenden Sie zum Angeben eines Satzes wiederholter Felder oder Gruppen, die eine unbestimmte Anzahl sind die **Select** -Methode der **XPathNavigator** -Klasse. Diese Methode gibt ein XPathNodeIterator-Objekt, das Sie, das zum Durchlaufen der Knoten der angegebenen Auflistung verwenden können zurück. 
  
Im folgende Beispiel wird davon ausgegangen, dass die Formularvorlage enthält, einer **Aufzählung** oder einer ähnlichen wiederholten Steuerelement, das an ein wiederholtes Element mit dem Namen gebunden ist `field1`. Der XPath-Ausdruck des Felds an die **Select** -Methode übergeben wird, und die zurückgegebene **XPathNodeIterator** zugeordnet ist, die `nodes` Variable. Verwenden Sie die MoveNext-Methode zum Durchlaufen der Auflistung von Knoten und die aktuelle-Eigenschaft, um ein auf dem aktuellen Knoten positioniert **XPathNavigator** -Objekt zurückzugeben. Verwenden Sie schließlich die **Value** -Eigenschaft zum Abrufen und Anzeigen des Werts jedes wiederholten Felds. 
  
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
  
Anstatt die **Value**-Eigenschaft zum Abrufen des Werts jeder Instanz des wiederholten Felds zu verwenden, können Sie auch mithilfe der**SetValue**-Methode die Felder durchlaufen und ihre Werte festlegen (siehe das folgende Beispiel). 
  
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

Zugriff auf eine externe Datenquelle, die dem Formular zugeordneten übergeben Sie den Namen der Datenquelle an die [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse. Zum Erstellen einer Verbindung mit einer neuen externen Datenquelle oder um eine Liste mit den Namen der vorhandenen externen datenquellenverbindungen anzuzeigen, klicken Sie auf der Registerkarte **Daten** des Menübands auf **Datenverbindungen** . 
  
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
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) -Methode  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) -Methode  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) -Eigenschaft  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) -Eigenschaft  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode  <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) -Methode  <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) -Methode  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) -Methode  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) -Methode  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) -Methode  <br/> |
|[Formerror-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methoden  <br/> |
|[Formularvorlage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) -Eigenschaft  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) -Eigenschaft  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) -Methode  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) (Eigenschaft)  <br/> |
|[SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) (Eigenschaft)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methoden  <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methoden  <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methoden  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) -Methode  <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) -Methode  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) -Eigenschaft  <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft, die ein **DataSource** -Objekt zurückgibt, die wiederum die **CreateNavigator** -Methode zum Erstellen eines **XPathNavigator** -Objekts im Stamm des dem Formular zugrunde liegenden XML-Dokument (Hauptdaten bereitstellt Quelle).  <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methoden  <br/> |
   
Neben den InfoPath-Objektmodellmembern, die ein **XPathNavigator**-Objekt zurückgeben oder annehmen, geben die folgenden Methoden eine Instanz der **XPathNodeIterator**-Klasse des **System.Xml.XPath**-Namespace zum Durchlaufen der XML-Knoten von Elementen zurück, die in einer Ansicht angegeben oder ausgewählt werden. 
  
|**Übergeordnete Klasse**|**Element**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methoden  <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Verwenden der Klassen "XPathNavigator" und "XPathNodeIterator" für in einer Ansicht ausgewählte Daten
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Im folgenden Beispiel werden Member der Klassen **XPathNavigator** und **XPathNodeIterator** für Formulardaten in der folgenden Reihenfolge verwendet: 
  
1. Die **CreateNavigator** -Methode der **DataSource** -Klasse dient zum Erstellen einer **XPathNavigator** -Objektvariable mit dem Namen repeatingTableRow1, die standardmäßig im Stammverzeichnis des zugrunde liegenden XML-Dokument des Formulars (die Hauptdaten positioniert ist Quelle).
    
2. Die **SelectSingleNode**-Methode der **XPathNavigator**-Klasse dient zum Verschieben der Position des **XPathNavigator**-Objekts in die erste Zeile des Steuerelements **Wiederholte Tabelle**, das an group2 in der Datenquelle gebunden ist. 
    
3. Die repeatingTableRow1-Objektvariable wird an die **SelectNodes**-Methode der **View**-Klasse übergeben, um die Knoten in dieser Zeile auszuwählen. 
    
4. Eine **XPathNodeIterator**-Objektvariable mit dem Namen selectedNodes wird deklariert, und die **GetSelectedNodes**-Methode der **View**-Klasse wird verwendet, um das **XPathNodeIterator**-Objekt mit den ausgewählten Knoten aufzufüllen.  
    
5. Die **Count**-Eigenschaft der **XPathNodeIterator**-Klasse dient zum Anzeigen der Anzahl der Knoten, die in der selectedNodes-Objektvariablen enthalten sind. 
    
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

Weitere Informationen zum Arbeiten mit XML-Daten aus InfoPath-Formularvorlagen finden Sie unter Arbeiten mit XML-Daten unter Verwendung der XPathNavigator-Klasse in InfoPath 2007-Formularvorlagen.
  

