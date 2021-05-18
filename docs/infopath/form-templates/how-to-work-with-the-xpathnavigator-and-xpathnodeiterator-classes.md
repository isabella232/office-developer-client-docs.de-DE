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
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="f5bc6-105">Arbeiten mit den Klassen XPathNavigator und XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="f5bc6-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="f5bc6-106">Um auf die XML-Daten in Formularvorlagendatenquellen zu zugreifen und diese zu bearbeiten, werden viele Elemente des objektmodells für verwalteten Code von [Microsoft.Office. InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) erstellt oder kann eine Instanz der **XPathNavigator-Klasse** des **System.Xml. XPath-Namespace.**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-106">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace.</span></span> <span data-ttu-id="f5bc6-107">Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt erhalten haben, das von einem InfoPath-Objektmodellmember zurückgegeben wird, können Sie die Eigenschaften und Methoden der **XPathNavigator**-Klasse verwenden, um mit den Daten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-107">After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="f5bc6-108">Das am häufigsten verwendete Mitglied der **Microsoft.Office. Der** InfoPath-Namespace, der die **XPathNavigator-Klasse** verwendet, ist die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) der [DataSource-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) mit der Sie mit den gespeicherten Daten arbeiten können, die durch ein **DataSource-Objekt** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-108">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object.</span></span> <span data-ttu-id="f5bc6-109">Von der **CreateNavigator**-Methode wird ein **XPathNavigator**-Objekt am Stamm der Datenquelle erstellt, die vom **DataSource**-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-109">The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="f5bc6-110">Wenn Sie mit der Verwendung von MSXML5 aus Skript zum Arbeiten mit Daten in Microsoft InfoPath 2003 vertraut sind, können Sie sich die **CreateNavigator**-Methode als Ersatz für die **DOM**-Eigenschaft von **DataObject** vorstellen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="f5bc6-111">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf die Hauptdatenquelle des Formulars</span><span class="sxs-lookup"><span data-stu-id="f5bc6-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="f5bc6-112">Um auf die Hauptdatenquelle des Formulars zu zugreifen, rufen Sie die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) direkt über das Schlüsselwort **C#** oder **Me** (Visual Basic) auf.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-112">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="f5bc6-113">Im folgenden Codebeispiel wird ein **XPathNavigator**-Objekt am Stamm der Hauptdatenquelle mithilfe der **CreateNavigator**-Methode erstellt, und dann wird die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-113">The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
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
> <span data-ttu-id="f5bc6-114">Das Aufrufen der [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) direkt aus dem **This-** oder **Me-Schlüsselwort** entspricht dem Aufrufen der [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) mithilfe der [MainDataSource-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( ) oder durch Übergeben einer leeren Zeichenfolge an die  `this.MainDataSource.CreateNavigator()` [DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()` ).</span><span class="sxs-lookup"><span data-stu-id="f5bc6-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="f5bc6-115">Auswählen und Festlegen der XML-Knoten für Felder in der Hauptdatenquelle</span><span class="sxs-lookup"><span data-stu-id="f5bc6-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="f5bc6-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="f5bc6-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="f5bc6-117">Verwenden Sie zum Auswählen des einzelnen XML-Knotens für ein Feld in einer Datenquelle die **SelectSingleNode(String,IXmlNamespaceResolver)-Methode** der **XPathNavigator-Klasse.**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-117">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="f5bc6-118">Wenn Sie mit einer Reihe wiederholter Felder oder wiederholter Gruppen arbeiten möchten, verwenden Sie die **Select(String,IXmlNamespaceResolver)-Methode** der **XPathNavigator-Klasse.**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-118">If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="f5bc6-119">Diese Methode gibt ein **XPathNodeIterator-Objekt zurück,** das eine Auflistung von Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-119">This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="f5bc6-120">Auswählen und Festlegen des Werts eines einzelnen Knotens</span><span class="sxs-lookup"><span data-stu-id="f5bc6-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="f5bc6-121">Die überladene **SelectSingleNode-Methode,** die Sie verwenden müssen, verfügt über einen  _xpath-Parameter,_ der einen XPath-Ausdruck als Zeichenfolge verwendet, und einen  _Resolverparameter,_ der ein **XmlNamespaceManager-Objekt** zum Auflösen von Namespacepräfixen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-121">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes.</span></span> <span data-ttu-id="f5bc6-122">Um einen einzelnen Knoten in der Hauptdatenquelle des Formulars auszuwählen, übergeben Sie einen XPath-Ausdruck, der das Feld oder die Gruppe angibt, die Sie für den  _xpath-Parameter_ auswählen möchten, zusammen mit dem **XmlNamespaceManager-Objekt,** das von der [NamespaceManager-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) des **XmlForm-Objekts zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-122">To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object.</span></span> <span data-ttu-id="f5bc6-123">Das zurückgegebene **XmlNamespaceManager**-Objekt wird mit allen Namespates, die in der Formulardefinitionsdatei (XSF) der Formularvorlage definiert sind, zum Ladezeitpunkt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-123">The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="f5bc6-p107">Die einfachste Möglichkeit zum Erstellen eines XPath-Ausdrucks zum Auswählen eines Knotens in der Datenquelle des Formulars ist das Klicken mit der rechten Maustaste im Aufgabenbereich **Felder** auf das Feld oder die Gruppe und anschließende Klicken auf **XPath kopieren**. Fügen Sie zum Erstellen und Testen manuell bearbeiteter XPath-Ausdrücke für den Zugriff auf Knoten in einem komplexen oder überaus geschachtelten XML-Schema dem Formular ein Steuerelement vom Typ **Ausdrucksfeld** hinzu. Geben Sie dann den XPath-Ausdruck für das Steuerelement an, und zeigen Sie anschließend eine Vorschau des Formulars an, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="f5bc6-126">Im folgenden Beispiel wird die **SelectSingleNode-Methode** verwendet, um den einzelnen Knoten für das Feld  `EmailAlias` auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-126">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field.</span></span> <span data-ttu-id="f5bc6-127">Anschließend wird die **SetValue-Methode** der **XPathNavigator-Klasse** und die [UserName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) der [User-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) verwendet, um den Wert des Felds auf den Alias des aktuellen Benutzers zu setzen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-127">Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
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

<span data-ttu-id="f5bc6-128">Informationen zum Erstellen von XPath-Ausdrücken finden Sie in der XPath-Referenz auf MSDN und in der [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="f5bc6-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="f5bc6-129">Festlegen des Werts eines Knotens mit dem Attribut "xsi:nil"</span><span class="sxs-lookup"><span data-stu-id="f5bc6-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="f5bc6-130">Bei bestimmten Datentypen wird beim Versuch, den Wert eines leeren Felds programmgesteuert festzulegen, der Fehler "Nicht datentypbezogene Fehler bei der Schemaüberprüfung" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-130">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors."</span></span> <span data-ttu-id="f5bc6-131">In der Regel ist die Ursache dieses Fehlers, dass für das Element das [xsi:nil-Attribut](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) auf **true festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-131">Typically the cause of this error is that the element has the [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**.</span></span> <span data-ttu-id="f5bc6-132">Wenn Sie das zugrunde liegende XML-Element des leeren Felds im Formular untersuchen, können Sie diese Einstellung erkennen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-132">If you examine the underlying XML element for the blank field in the form, you can see this setting.</span></span> <span data-ttu-id="f5bc6-133">Im XML-Fragment des folgenden leeren "Date"-Felds ist z. B. das **xsi:nil**-Attribute auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-133">For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="f5bc6-134">Wenn das **xsi:nil-Attribut** auf **true** festgelegt ist, gibt es an, dass das Element vorhanden ist, aber keinen Wert hat, oder anders ausgedrückt, null ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-134">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null .</span></span> <span data-ttu-id="f5bc6-135">Wenn Sie versuchen, den Wert eines solchen Knotens programmgesteuert zu setzen, zeigt InfoPath die Meldung "Schemaüberprüfung gefundene Nicht-Datentypfehler" an, da das Element derzeit als null gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-135">If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null .</span></span> <span data-ttu-id="f5bc6-136">InfoPath legt das **xsi:nil**-Attribut für null-Felder der folgenden Datentypen auf **true** fest:</span><span class="sxs-lookup"><span data-stu-id="f5bc6-136">InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="f5bc6-137">**Ganze Zahl (ganze Zahl)**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="f5bc6-138">**Decimal (double)**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="f5bc6-139">**Datum (Datum)**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-139">**Date (date)**</span></span>
    
- <span data-ttu-id="f5bc6-140">**Zeit (Zeit)**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-140">**Time (time)**</span></span>
    
- <span data-ttu-id="f5bc6-141">**Datum und Uhrzeit (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="f5bc6-p111">Zum Vermeiden dieses Fehlers muss Ihr Code prüfen, ob das **xsi:nil**-Attribut vorhanden ist, und falls ja, es entfernen, bevor der Wert des Knotens festgelegt wird. Die folgende Unterroutine verwendet ein **XpathNavigator**-Objekt am Knoten, den Sie festlegen möchten, sucht nach dem **nil**-Attribut und löscht es, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-p111">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node. The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
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

<span data-ttu-id="f5bc6-144">Sie können diese Unterroutine aufrufen, bevor Sie versuchen, ein Feld eines Datentyps festzulegen, das ggf. das **xsi:nil**-Attribut aufweist (siehe das folgende Beispiel, das ein "Date"-Feld festlegt).</span><span class="sxs-lookup"><span data-stu-id="f5bc6-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
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
> <span data-ttu-id="f5bc6-145">Obwohl die Implementierung des **XPathNavigator-Objekts** in InfoPath die **SetTypedValue-Methode** verfügbar macht, die zum Festlegen eines Knotens mithilfe eines bestimmten Typs verwendet wird, implementiert InfoPath diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-145">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method.</span></span> <span data-ttu-id="f5bc6-146">Sie müssen stattdessen die **SetValue**-Methode verwenden und einen Zeichenfolgenwert im ordnungsgemäßen Format für den Datentyp des Knotens übergeben.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-146">You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="f5bc6-147">Auswählen und Festlegen eines Satzes wiederholter Knoten</span><span class="sxs-lookup"><span data-stu-id="f5bc6-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="f5bc6-148">Verwenden Sie die **Select-Methode** der **XPathNavigator-Klasse,** um einen Satz wiederholter Felder oder Gruppen anzugeben, die einer unbestimmten Zahl entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="f5bc6-149">Diese Methode gibt ein XPathNodeIterator-Objekt zurück, mit dem Sie die angegebene Auflistung von Knoten durch iterieren können.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="f5bc6-150">Im folgenden Beispiel wird davon ausgegangen, dass Ihre Formularvorlage ein Aufzählungszeichen oder ein ähnliches wiederholtes Steuerelement enthält, das an ein wiederholtes Element namens gebunden  `field1` ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="f5bc6-151">Der XPath des Felds wird an die **Select-Methode** übergeben, und der zurückgegebene **XPathNodeIterator** wird der Variablen  `nodes` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="f5bc6-152">Sie verwenden die MoveNext-Methode, um die Auflistung von Knoten zu durch iterieren, und die Current-Eigenschaft gibt ein **XPathNavigator-Objekt** zurück, das auf dem aktuellen Knoten positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="f5bc6-153">Verwenden Sie schließlich die **Value-Eigenschaft,** um den Wert jedes wiederholten Felds abzurufen und zu anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
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

<span data-ttu-id="f5bc6-p115">Das vorherige Beispiel funktioniert mit Zeichenfolgenwerten im angegebenen wiederholten Feld. Wenn das Feld jedoch numerische Werte enthält, können Sie ähnlichen Code verwenden, um die Werte im Feld für Berechnungen, z. B. der Summe der Werte oder ihres Durchschnitts, zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="f5bc6-156">Anstatt die **Value**-Eigenschaft zum Abrufen des Werts jeder Instanz des wiederholten Felds zu verwenden, können Sie auch mithilfe der **SetValue**-Methode die Felder durchlaufen und ihre Werte festlegen (siehe das folgende Beispiel).</span><span class="sxs-lookup"><span data-stu-id="f5bc6-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="f5bc6-157">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf eine externe Datenquelle</span><span class="sxs-lookup"><span data-stu-id="f5bc6-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="f5bc6-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="f5bc6-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="f5bc6-159">Um auf eine externe Datenquelle zu zugreifen, die dem Formular zugeordnet ist, übergeben Sie den Namen der Datenquelle an die [DataSources-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) der [XmlForm-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-159">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="f5bc6-160">Klicken Sie zum Herstellen einer Verbindung mit einer neuen externen Datenquelle oder zum Anzeigen einer Liste der Namen der vorhandenen Verbindungen mit externen Datenquellen im Menüband auf der Registerkarte **Daten** auf **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-160">To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="f5bc6-p117">Im folgenden Codebeispiel wird gezeigt, wie ein **XPathNavigator**-Objekt am Stamm einer externen Datenquelle mit dem Namen "CityList" mithilfe der **CreateNavigator**-Methode erstellt wird und dann die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet wird, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen. Dieses Codebeispiel geht davon aus, dass Sie eine Datenverbindung mit einer Liste von Ortsnamen erstellt haben, die in einer externen Datenquelle gespeichert sind, z. B. in einem XML-Dokument oder einer SharePoint-Liste, und die Datenverbindung "CityList" genannt haben.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-p117">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box. This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
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

<span data-ttu-id="f5bc6-163">Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt am Stamm der externen Datenquelle erhalten haben, können Sie mithilfe von Members der **XPathNavigator**-Klasse wie den Methoden **SelectSingleNode** und **SetValue** mit den enthaltenen Daten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="f5bc6-164">InfoPath-Objektmodellmember, von denen die Klassen "XPathNavigator" und "XPathNodeIterator" verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f5bc6-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="f5bc6-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="f5bc6-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="f5bc6-166">Die folgende Tabelle enthält eine Übersicht aller Member des **Microsoft.Office.InfoPath**-Namespace, von denen die **XPathNavigator**-Klasse verwendet wird, um auf XML-Daten zuzugreifen, sie zu bearbeiten oder zu senden.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="f5bc6-167">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-167">**Parent Class**</span></span>|<span data-ttu-id="f5bc6-168">**Element**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5bc6-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="f5bc6-170">[BuildSqlFromXmlNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="f5bc6-172">[BuildSqlFromXmlNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5bc6-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="f5bc6-174">[Source-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5bc6-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="f5bc6-176">[Context-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-177">DataSource</span><span class="sxs-lookup"><span data-stu-id="f5bc6-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="f5bc6-178">[CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="f5bc6-179">[GetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="f5bc6-180">[SetNamedNodeProperty-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="f5bc6-182">[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="f5bc6-184">[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="f5bc6-186">[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-187">FormError</span><span class="sxs-lookup"><span data-stu-id="f5bc6-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="f5bc6-188">[Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="f5bc6-190">[Hinzufügen von](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) Methoden</span><span class="sxs-lookup"><span data-stu-id="f5bc6-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-191">FormTemplate</span><span class="sxs-lookup"><span data-stu-id="f5bc6-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="f5bc6-192">[Manifest-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5bc6-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="f5bc6-194">[Xml-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="f5bc6-196">[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-197">Signatur</span><span class="sxs-lookup"><span data-stu-id="f5bc6-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="f5bc6-198">[SignatureBlockXmlNode-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="f5bc6-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="f5bc6-200">[SignatureContainer-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-201">View</span><span class="sxs-lookup"><span data-stu-id="f5bc6-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="f5bc6-202">[GetContextNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="f5bc6-203">[SelectNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="f5bc6-204">[SelectText-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="f5bc6-206">[Execute-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="f5bc6-207">[GenerateDataSetDiffGram-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5bc6-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="f5bc6-209">[OldParent-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="f5bc6-210">[Site-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="f5bc6-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="f5bc6-212">[MainDataSource-Eigenschaft,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) die ein **DataSource-Objekt** zurückgibt, das wiederum die **CreateNavigator-Methode** zum Erstellen eines **XPathNavigator-Objekts** am Stamm des dem Formular zugrunde liegenden XML-Dokuments (Hauptdatenquelle) zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="f5bc6-213">[MergeForm-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="f5bc6-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="f5bc6-215">[NewFromFormTemplate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="f5bc6-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f5bc6-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="f5bc6-217">[ReportError-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="f5bc6-218">Neben den InfoPath-Objektmodellmembern, die ein **XPathNavigator**-Objekt zurückgeben oder annehmen, geben die folgenden Methoden eine Instanz der **XPathNodeIterator**-Klasse des **System.Xml.XPath**-Namespace zum Durchlaufen der XML-Knoten von Elementen zurück, die in einer Ansicht angegeben oder ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="f5bc6-219">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-219">**Parent Class**</span></span>|<span data-ttu-id="f5bc6-220">**Element**</span><span class="sxs-lookup"><span data-stu-id="f5bc6-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5bc6-221">View</span><span class="sxs-lookup"><span data-stu-id="f5bc6-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="f5bc6-222">[GetContextNodes-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="f5bc6-223">[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5bc6-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="f5bc6-224">Verwenden der Klassen "XPathNavigator" und "XPathNodeIterator" für in einer Ansicht ausgewählte Daten</span><span class="sxs-lookup"><span data-stu-id="f5bc6-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="f5bc6-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="f5bc6-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span></span>

<span data-ttu-id="f5bc6-226">Im folgenden Beispiel werden Member der Klassen **XPathNavigator** und **XPathNodeIterator** für Formulardaten in der folgenden Reihenfolge verwendet:</span><span class="sxs-lookup"><span data-stu-id="f5bc6-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="f5bc6-227">Die **CreateNavigator-Methode** der **DataSource-Klasse** wird zum Erstellen einer **XPathNavigator-Objektvariablen** namens repeatingTableRow1 verwendet, die standardmäßig am Stamm des zugrunde liegenden XML-Dokuments des Formulars (der Hauptdatenquelle) positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="f5bc6-228">Die **SelectSingleNode-Methode** der **XPathNavigator-Klasse** wird verwendet, um die Position des **XPathNavigator-Objekts** in die erste Zeile eines **Steuerelements** für wiederholte Tabelle zu verschieben, das an Group2 in der Datenquelle gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="f5bc6-229">Die repeatingTableRow1-Objektvariable wird an die **SelectNodes**-Methode der **View**-Klasse übergeben, um die Knoten in dieser Zeile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="f5bc6-230">Eine **XPathNodeIterator-Objektvariable** namens selectedNodes wird deklariert, und die **GetSelectedNodes-Methode** der **View-Klasse** wird verwendet, um das **XPathNodeIterator-Objekt** mit den ausgewählten Knoten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="f5bc6-231">Mit **der Count-Eigenschaft** der **XPathNodeIterator-Klasse** wird die Anzahl der Knoten angezeigt, die in der selectedNodes-Objektvariablen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="f5bc6-232">Eine For/Each-Schleife dient zum Durchlaufen der Knoten in der selectedNodes-Objektvariablen und zum Anzeigen von Informationen zu den einzelnen Knoten mithilfe der Eigenschaften **Name**, **InnerXml** und **Value** der **XPathNavigator**-Klasse.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
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

<span data-ttu-id="f5bc6-233">Weitere Informationen zum Arbeiten mit XML-Daten aus InfoPath-Formularvorlagen finden Sie unter Arbeiten mit XML-Daten mithilfe der XPathNavigator-Klasse in InfoPath 2007-Formularvorlagen.</span><span class="sxs-lookup"><span data-stu-id="f5bc6-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

