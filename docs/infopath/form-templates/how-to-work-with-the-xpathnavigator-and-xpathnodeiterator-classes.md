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
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="ff287-105">Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"</span><span class="sxs-lookup"><span data-stu-id="ff287-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="ff287-106">Zugriff und zum Bearbeiten der XML-Datenteils im Formular Vorlage Datenquellen, viele Mitglieder der vom [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellten Objektmodell für verwalteten Code erstellen oder eine Instanz der **XPathNavigator** -Klasse übergeben werden kann die **Auswertungsmodul** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="ff287-106">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace.</span></span> <span data-ttu-id="ff287-107">Nachdem Sie den Zugriff auf ein **XPathNavigator** -Objekt zurückgegeben, die durch ein InfoPath-Objektmodellmember haben, können Sie die Eigenschaften und Methoden der **XPathNavigator** -Klasse zum Arbeiten mit den Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff287-107">After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="ff287-108">Der am häufigsten verwendete Member des **Microsoft.Office.InfoPath** -Namespace, der die **XPathNavigator** -Klasse verwendet wird, die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse, die Sie mit den gespeicherten Daten arbeiten können durch ein **DataSource** -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ff287-108">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object.</span></span> <span data-ttu-id="ff287-109">Die **CreateNavigator** -Methode erstellt ein am Stamm der durch das **DataSource** -Objekt dargestellte Datenquelle positioniertes **XPathNavigator** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff287-109">The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ff287-110">Wenn Sie mit der Verwendung von MSXML5 aus Skript zum Arbeiten mit Daten in Microsoft InfoPath 2003 vertraut sind, können Sie sich die **CreateNavigator**-Methode als Ersatz für die **DOM**-Eigenschaft von **DataObject** vorstellen.</span><span class="sxs-lookup"><span data-stu-id="ff287-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="ff287-111">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf die Hauptdatenquelle des Formulars</span><span class="sxs-lookup"><span data-stu-id="ff287-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="ff287-112">Rufen Sie den Zugriff auf die Hauptdatenquelle des Formulars die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode direkt über das **dieses** (c#) oder Schlüsselwort **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="ff287-112">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="ff287-113">Im folgende Beispiel ein **XPathNavigator** -Objekts am Stamm der Hauptdatenquelle mithilfe der **CreateNavigator** -Methode erstellt, und klicken Sie dann die **OuterXml** -Eigenschaft der **XPathNavigator** -Klasse verwendet, um die XML-Daten anzeigen in einem Meldungsfeld zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff287-113">The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
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
> <span data-ttu-id="ff287-114">Aufrufen von die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode direkt über das **this** oder **Me** -Schlüsselwort ist gleichbedeutend mit dem [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode mit der [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft ( `this.MainDataSource.CreateNavigator()`) oder indem Sie eine leere Zeichenfolge an die [ DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse ( `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="ff287-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="ff287-115">Auswählen und Festlegen der XML-Knoten für Felder in der Hauptdatenquelle</span><span class="sxs-lookup"><span data-stu-id="ff287-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="ff287-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="ff287-116"></span></span>

<span data-ttu-id="ff287-117">Um die einzelnen XML-Knoten für ein Feld in einer Datenquelle auswählen möchten, verwenden Sie die **SelectSingleNode(String,IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff287-117">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="ff287-118">Wenn Sie mit einem Satz von wiederholte Felder oder wiederholte Gruppen arbeiten möchten, verwenden Sie die **Select(String,IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff287-118">If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="ff287-119">Diese Methode gibt ein **XPathNodeIterator** -Objekt, das eine Auflistung von Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff287-119">This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="ff287-120">Auswählen und Festlegen des Werts eines einzelnen Knotens</span><span class="sxs-lookup"><span data-stu-id="ff287-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="ff287-121">Die überladene **SelectSingleNode** -Methode, die Sie verwenden müssen verfügt über einen _Xpath_ -Parameter, der einen XPath-Ausdruck als Zeichenfolge annimmt, und einen _Auflösung_ -Parameter, der ein **XmlNamespaceManager** -Objekt für die Beilegung von Namespace akzeptiert Präfixe.</span><span class="sxs-lookup"><span data-stu-id="ff287-121">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes.</span></span> <span data-ttu-id="ff287-122">Um einen einzelnen Knoten in der Hauptdatenquelle des Formulars auszuwählen, übergeben Sie einen XPath-Ausdruck, der angibt, das Feld oder Gruppe, die Sie für den _Xpath_ -Parameter zusammen mit dem **XmlNamespaceManager** -Objekt auswählen möchten, die von der [zurückgegeben wird NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) -Eigenschaft der **XmlForm** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff287-122">To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object.</span></span> <span data-ttu-id="ff287-123">Das zurückgegebene **XmlNamespaceManager** -Objekt wird zur Ladezeit mit allen Namespaces initialisiert, die von der Formulardefinitionsdatei (XSF) der Formularvorlage definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff287-123">The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="ff287-p107">Die einfachste Möglichkeit zum Erstellen eines XPath-Ausdrucks zum Auswählen eines Knotens in der Datenquelle des Formulars ist das Klicken mit der rechten Maustaste im Aufgabenbereich **Felder** auf das Feld oder die Gruppe und anschließende Klicken auf **XPath kopieren**. Fügen Sie zum Erstellen und Testen manuell bearbeiteter XPath-Ausdrücke für den Zugriff auf Knoten in einem komplexen oder überaus geschachtelten XML-Schema dem Formular ein Steuerelement vom Typ **Ausdrucksfeld** hinzu. Geben Sie dann den XPath-Ausdruck für das Steuerelement an, und zeigen Sie anschließend eine Vorschau des Formulars an, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff287-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="ff287-126">Das folgende Beispiel verwendet die **SelectSingleNode** -Methode für den einzelnen Knoten aus der `EmailAlias` dar.</span><span class="sxs-lookup"><span data-stu-id="ff287-126">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field.</span></span> <span data-ttu-id="ff287-127">Anschließend werden die **SetValue** -Methode der **XPathNavigator** -Klasse und die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse für den Wert des Felds festzulegen, den Alias des aktuellen Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff287-127">Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
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

<span data-ttu-id="ff287-128">Informationen zum Erstellen von XPath-Ausdrücken finden Sie unter der XPath-Referenz auf MSDN und die [Empfehlung für XML Path Language (XPath) Version 1.0 W3C](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="ff287-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="ff287-129">Festlegen des Werts eines Knotens mit dem Attribut "xsi:nil"</span><span class="sxs-lookup"><span data-stu-id="ff287-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="ff287-130">Für bestimmte Datentypen wird versucht, den Wert eines leeren Feldes programmgesteuert festlegen der Fehler "schemavalidierung wurden nicht vom Datentyp Fehler gefunden."</span><span class="sxs-lookup"><span data-stu-id="ff287-130">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors."</span></span> <span data-ttu-id="ff287-131">In der Regel ist die Ursache für diesen Fehler an, dass das Element das [xsi: nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) -Attribut auf **true**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff287-131">Typically the cause of this error is that the element has the [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**.</span></span> <span data-ttu-id="ff287-132">Wenn Sie das zugrunde liegende XML-Element für das leere Feld in der Form untersuchen, können Sie diese Einstellung finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="ff287-132">If you examine the underlying XML element for the blank field in the form, you can see this setting.</span></span> <span data-ttu-id="ff287-133">Das XML-Fragment für die folgenden leeren Datumsfeld verfügt beispielsweise über das **xsi: nil** -Attribut auf **true**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ff287-133">For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="ff287-134">Wenn das **xsi: nil** -Attribut auf **true**festgelegt ist, bedeutet dies, dass das Element vorhanden ist, jedoch wird kein Wert oder mit anderen Worten, null ist.</span><span class="sxs-lookup"><span data-stu-id="ff287-134">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null .</span></span> <span data-ttu-id="ff287-135">Wenn Sie versuchen, den Wert eines solchen Knotens programmgesteuert festlegen, zeigt InfoPath die Meldung "schemavalidierung found nicht-Datentyp-Fehler" an, da das Element derzeit als null gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff287-135">If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null .</span></span> <span data-ttu-id="ff287-136">InfoPath legt das **xsi: nil** -Attribut auf **true** für null-Felder der folgenden Datentypen:</span><span class="sxs-lookup"><span data-stu-id="ff287-136">InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="ff287-137">**Ganze Zahl (Integer)**</span><span class="sxs-lookup"><span data-stu-id="ff287-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="ff287-138">**Dezimalzahl (Double)**</span><span class="sxs-lookup"><span data-stu-id="ff287-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="ff287-139">**Datum (Date)**</span><span class="sxs-lookup"><span data-stu-id="ff287-139">**Date (date)**</span></span>
    
- <span data-ttu-id="ff287-140">**Uhrzeit)**</span><span class="sxs-lookup"><span data-stu-id="ff287-140">**Time (time)**</span></span>
    
- <span data-ttu-id="ff287-141">**Datum und Uhrzeit (DateTime)**</span><span class="sxs-lookup"><span data-stu-id="ff287-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="ff287-p111">Zum Vermeiden dieses Fehlers muss Ihr Code prüfen, ob das **xsi:nil**-Attribut vorhanden ist, und falls ja, es entfernen, bevor der Wert des Knotens festgelegt wird. Die folgende Unterroutine verwendet ein **XpathNavigator**-Objekt am Knoten, den Sie festlegen möchten, sucht nach dem **nil**-Attribut und löscht es, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ff287-p111">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node. The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
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

<span data-ttu-id="ff287-144">Sie können diese Unterroutine aufrufen, bevor Sie versuchen, ein Feld eines Datentyps festzulegen, das ggf. das **xsi:nil**-Attribut aufweist (siehe das folgende Beispiel, das ein "Date"-Feld festlegt).</span><span class="sxs-lookup"><span data-stu-id="ff287-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
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
> <span data-ttu-id="ff287-145">Obwohl die Implementierung der **XPathNavigator** -Objekt in InfoPath die **SetTypedValue** -Methode verfügbar macht – die wird verwendet, um einen Knoten mit einem Wert eines bestimmten Typs festlegen – InfoPath diese Methode nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ff287-145">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method.</span></span> <span data-ttu-id="ff287-146">Sie müssen stattdessen die **SetValue** -Methode, und übergeben Sie einen String-Wert, der das richtige Format für den Datentyp des Knotens.</span><span class="sxs-lookup"><span data-stu-id="ff287-146">You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="ff287-147">Auswählen und Festlegen eines Satzes wiederholter Knoten</span><span class="sxs-lookup"><span data-stu-id="ff287-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="ff287-148">Verwenden Sie zum Angeben eines Satzes wiederholter Felder oder Gruppen, die eine unbestimmte Anzahl sind die **Select** -Methode der **XPathNavigator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff287-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="ff287-149">Diese Methode gibt ein XPathNodeIterator-Objekt, das Sie, das zum Durchlaufen der Knoten der angegebenen Auflistung verwenden können zurück.</span><span class="sxs-lookup"><span data-stu-id="ff287-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="ff287-150">Im folgende Beispiel wird davon ausgegangen, dass die Formularvorlage enthält, einer **Aufzählung** oder einer ähnlichen wiederholten Steuerelement, das an ein wiederholtes Element mit dem Namen gebunden ist `field1`.</span><span class="sxs-lookup"><span data-stu-id="ff287-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="ff287-151">Der XPath-Ausdruck des Felds an die **Select** -Methode übergeben wird, und die zurückgegebene **XPathNodeIterator** zugeordnet ist, die `nodes` Variable.</span><span class="sxs-lookup"><span data-stu-id="ff287-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="ff287-152">Verwenden Sie die MoveNext-Methode zum Durchlaufen der Auflistung von Knoten und die aktuelle-Eigenschaft, um ein auf dem aktuellen Knoten positioniert **XPathNavigator** -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff287-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="ff287-153">Verwenden Sie schließlich die **Value** -Eigenschaft zum Abrufen und Anzeigen des Werts jedes wiederholten Felds.</span><span class="sxs-lookup"><span data-stu-id="ff287-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
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

<span data-ttu-id="ff287-p115">Das vorherige Beispiel funktioniert mit Zeichenfolgenwerten im angegebenen wiederholten Feld. Wenn das Feld jedoch numerische Werte enthält, können Sie ähnlichen Code verwenden, um die Werte im Feld für Berechnungen, z. B. der Summe der Werte oder ihres Durchschnitts, zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ff287-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="ff287-156">Anstatt die **Value**-Eigenschaft zum Abrufen des Werts jeder Instanz des wiederholten Felds zu verwenden, können Sie auch mithilfe der**SetValue**-Methode die Felder durchlaufen und ihre Werte festlegen (siehe das folgende Beispiel).</span><span class="sxs-lookup"><span data-stu-id="ff287-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="ff287-157">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf eine externe Datenquelle</span><span class="sxs-lookup"><span data-stu-id="ff287-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="ff287-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="ff287-158"></span></span>

<span data-ttu-id="ff287-159">Zugriff auf eine externe Datenquelle, die dem Formular zugeordneten übergeben Sie den Namen der Datenquelle an die [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff287-159">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="ff287-160">Zum Erstellen einer Verbindung mit einer neuen externen Datenquelle oder um eine Liste mit den Namen der vorhandenen externen datenquellenverbindungen anzuzeigen, klicken Sie auf der Registerkarte **Daten** des Menübands auf **Datenverbindungen** .</span><span class="sxs-lookup"><span data-stu-id="ff287-160">To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="ff287-p117">Im folgenden Codebeispiel wird gezeigt, wie ein **XPathNavigator**-Objekt am Stamm einer externen Datenquelle mit dem Namen "CityList" mithilfe der **CreateNavigator**-Methode erstellt wird und dann die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet wird, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen. Dieses Codebeispiel geht davon aus, dass Sie eine Datenverbindung mit einer Liste von Ortsnamen erstellt haben, die in einer externen Datenquelle gespeichert sind, z. B. in einem XML-Dokument oder einer SharePoint-Liste, und die Datenverbindung "CityList" genannt haben.</span><span class="sxs-lookup"><span data-stu-id="ff287-p117">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box. This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
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

<span data-ttu-id="ff287-163">Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt am Stamm der externen Datenquelle erhalten haben, können Sie mithilfe von Members der **XPathNavigator**-Klasse wie den Methoden **SelectSingleNode** und **SetValue** mit den enthaltenen Daten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff287-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="ff287-164">InfoPath-Objektmodellmember, von denen die Klassen "XPathNavigator" und "XPathNodeIterator" verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ff287-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="ff287-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="ff287-165"></span></span>

<span data-ttu-id="ff287-166">Die folgende Tabelle enthält eine Übersicht aller Member des **Microsoft.Office.InfoPath**-Namespace, von denen die **XPathNavigator**-Klasse verwendet wird, um auf XML-Daten zuzugreifen, sie zu bearbeiten oder zu senden.</span><span class="sxs-lookup"><span data-stu-id="ff287-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="ff287-167">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff287-167">**Parent Class**</span></span>|<span data-ttu-id="ff287-168">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff287-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff287-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="ff287-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="ff287-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ff287-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="ff287-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ff287-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="ff287-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-177">DataSource</span><span class="sxs-lookup"><span data-stu-id="ff287-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="ff287-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="ff287-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="ff287-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="ff287-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="ff287-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="ff287-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-187">Formerror-Objekts</span><span class="sxs-lookup"><span data-stu-id="ff287-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="ff287-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="ff287-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="ff287-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="ff287-191">Formularvorlage</span><span class="sxs-lookup"><span data-stu-id="ff287-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="ff287-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="ff287-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="ff287-194">[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="ff287-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-197">Signature</span><span class="sxs-lookup"><span data-stu-id="ff287-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="ff287-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff287-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-199">SignedDataBlock-Objekt</span><span class="sxs-lookup"><span data-stu-id="ff287-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="ff287-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff287-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-201">View</span><span class="sxs-lookup"><span data-stu-id="ff287-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="ff287-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="ff287-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="ff287-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="ff287-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ff287-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="ff287-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="ff287-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="ff287-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="ff287-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="ff287-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff287-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="ff287-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="ff287-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="ff287-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft, die ein **DataSource** -Objekt zurückgibt, die wiederum die **CreateNavigator** -Methode zum Erstellen eines **XPathNavigator** -Objekts im Stamm des dem Formular zugrunde liegenden XML-Dokument (Hauptdaten bereitstellt Quelle).</span><span class="sxs-lookup"><span data-stu-id="ff287-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="ff287-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="ff287-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="ff287-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="ff287-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="ff287-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="ff287-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="ff287-218">Neben den InfoPath-Objektmodellmembern, die ein **XPathNavigator**-Objekt zurückgeben oder annehmen, geben die folgenden Methoden eine Instanz der **XPathNodeIterator**-Klasse des **System.Xml.XPath**-Namespace zum Durchlaufen der XML-Knoten von Elementen zurück, die in einer Ansicht angegeben oder ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ff287-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="ff287-219">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff287-219">**Parent Class**</span></span>|<span data-ttu-id="ff287-220">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff287-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff287-221">View</span><span class="sxs-lookup"><span data-stu-id="ff287-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="ff287-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="ff287-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="ff287-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="ff287-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="ff287-224">Verwenden der Klassen "XPathNavigator" und "XPathNodeIterator" für in einer Ansicht ausgewählte Daten</span><span class="sxs-lookup"><span data-stu-id="ff287-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="ff287-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="ff287-225"></span></span>

<span data-ttu-id="ff287-226">Im folgenden Beispiel werden Member der Klassen **XPathNavigator** und **XPathNodeIterator** für Formulardaten in der folgenden Reihenfolge verwendet:</span><span class="sxs-lookup"><span data-stu-id="ff287-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="ff287-227">Die **CreateNavigator** -Methode der **DataSource** -Klasse dient zum Erstellen einer **XPathNavigator** -Objektvariable mit dem Namen repeatingTableRow1, die standardmäßig im Stammverzeichnis des zugrunde liegenden XML-Dokument des Formulars (die Hauptdaten positioniert ist Quelle).</span><span class="sxs-lookup"><span data-stu-id="ff287-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="ff287-228">Die **SelectSingleNode**-Methode der **XPathNavigator**-Klasse dient zum Verschieben der Position des **XPathNavigator**-Objekts in die erste Zeile des Steuerelements **Wiederholte Tabelle**, das an group2 in der Datenquelle gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="ff287-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="ff287-229">Die repeatingTableRow1-Objektvariable wird an die **SelectNodes**-Methode der **View**-Klasse übergeben, um die Knoten in dieser Zeile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ff287-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="ff287-230">Eine **XPathNodeIterator**-Objektvariable mit dem Namen selectedNodes wird deklariert, und die **GetSelectedNodes**-Methode der **View**-Klasse wird verwendet, um das **XPathNodeIterator**-Objekt mit den ausgewählten Knoten aufzufüllen. </span><span class="sxs-lookup"><span data-stu-id="ff287-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="ff287-231">Die **Count**-Eigenschaft der **XPathNodeIterator**-Klasse dient zum Anzeigen der Anzahl der Knoten, die in der selectedNodes-Objektvariablen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ff287-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="ff287-232">Eine For/Each-Schleife dient zum Durchlaufen der Knoten in der selectedNodes-Objektvariablen und zum Anzeigen von Informationen zu den einzelnen Knoten mithilfe der Eigenschaften **Name**, **InnerXml** und **Value** der **XPathNavigator**-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ff287-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
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

<span data-ttu-id="ff287-233">Weitere Informationen zum Arbeiten mit XML-Daten aus InfoPath-Formularvorlagen finden Sie unter Arbeiten mit XML-Daten unter Verwendung der XPathNavigator-Klasse in InfoPath 2007-Formularvorlagen.</span><span class="sxs-lookup"><span data-stu-id="ff287-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

