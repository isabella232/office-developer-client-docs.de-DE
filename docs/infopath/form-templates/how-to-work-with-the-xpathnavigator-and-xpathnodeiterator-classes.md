---
title: Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- XPathNodeIterator-Klasse [InfoPath 2007], XPathNavigator-Klasse [InfoPath 2007], Formular-XML-Daten [InfoPath 2007], zugreifen auf, XML-DOM [InfoPath 2007], Konvertieren von MSXML5-Skripts [InfoPath 2007], MSXML5-Skript [InfoPath 2007], konvertieren
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Zum Zugreifen auf und Bearbeiten der XML-Daten in Formularvorlagen Datenquellen können viele Member des vom Microsoft. Office. InfoPath-Namespace bereitgestellten verwalteten Codeobjekt Modells entweder eine Instanz der XPathNavigator-Klasse von System. Xml. XPath erstellen oder übergeben. Namespace. Wenn Sie Zugriff auf einXPathNavigator-Objekt erhalten haben, das von einem InfoPath-Objektmodellmember zurückgegeben wird, können Sie die Eigenschaften und Methoden der XPathNavigator-Klasse verwenden, um mit den Daten zu arbeiten.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303549"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="cb469-105">Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"</span><span class="sxs-lookup"><span data-stu-id="cb469-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="cb469-106">Zum Zugreifen auf und Bearbeiten der XML-Daten in Formularvorlagen Datenquellen können viele Member des vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellten verwalteten Codeobjekt Modells entweder eine Instanz der **XPathNavigator** -Klasse des **System. Xml. XPath** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="cb469-106">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace.</span></span> <span data-ttu-id="cb469-107">Wenn Sie Zugriff auf ein**XPathNavigator**-Objekt erhalten haben, das von einem InfoPath-Objektmodellmember zurückgegeben wird, können Sie die Eigenschaften und Methoden der **XPathNavigator**-Klasse verwenden, um mit den Daten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb469-107">After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="cb469-108">Das am häufigsten verwendete Element des **Microsoft. Office. InfoPath** -Namespace, der die **XPathNavigator** -Klasse verwendet, ist die createNavigator-Methode der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse, mit der Sie mit den gespeicherten Daten arbeiten können. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) durch ein **DataSource** -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb469-108">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object.</span></span> <span data-ttu-id="cb469-109">Von der **CreateNavigator**-Methode wird ein **XPathNavigator**-Objekt am Stamm der Datenquelle erstellt, die vom **DataSource**-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb469-109">The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="cb469-110">Wenn Sie mit der Verwendung von MSXML5 aus Skript zum Arbeiten mit Daten in Microsoft InfoPath 2003 vertraut sind, können Sie sich die **CreateNavigator**-Methode als Ersatz für die **DOM**-Eigenschaft von **DataObject** vorstellen.</span><span class="sxs-lookup"><span data-stu-id="cb469-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="cb469-111">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf die Hauptdatenquelle des Formulars</span><span class="sxs-lookup"><span data-stu-id="cb469-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="cb469-112">Um auf die Hauptdatenquelle des Formulars zuzugreifen, rufen [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) Sie die CreateNavigator-Methode direkt im Schlüsselwort **this** (C#) oder **Me** (Visual Basic) auf.</span><span class="sxs-lookup"><span data-stu-id="cb469-112">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="cb469-113">Im folgenden Codebeispiel wird ein **XPathNavigator**-Objekt am Stamm der Hauptdatenquelle mithilfe der **CreateNavigator**-Methode erstellt, und dann wird die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb469-113">The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
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
> <span data-ttu-id="cb469-114">Das Aufrufen [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) der CreateNavigator-Methode direkt aus dem Schlüsselwort **this** oder **Me** entspricht dem Aufrufen der CreateNavigator-Methode mithilfe der `this.MainDataSource.CreateNavigator()` [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft () oder durch Übergeben einer leeren Zeichenfolge an den [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) [ ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)DataSources-Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse ( `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="cb469-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="cb469-115">Auswählen und Festlegen der XML-Knoten für Felder in der Hauptdatenquelle</span><span class="sxs-lookup"><span data-stu-id="cb469-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="cb469-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="cb469-116"></span></span>

<span data-ttu-id="cb469-117">Zum Auswählen des einzelnen XML-Knotens für ein Feld in einer Datenquelle verwenden Sie die **SelectSingleNode (String, IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="cb469-117">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="cb469-118">Wenn Sie mit einer Reihe von wiederholten Feldern oder wiederholten Gruppen arbeiten möchten, verwenden Sie die **Select (String, IXmlNamespaceResolver)** -Methode der **XPathNavigator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="cb469-118">If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="cb469-119">Diese Methode gibt ein **XPathNodeIterator** -Objekt zurück, das eine Auflistung von Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb469-119">This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="cb469-120">Auswählen und Festlegen des Werts eines einzelnen Knotens</span><span class="sxs-lookup"><span data-stu-id="cb469-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="cb469-121">Die überladene **SelectSingleNode** -Methode, die Sie verwenden müssen, verfügt über einen _XPath_ -Parameter, der einen XPath-Ausdruck als Zeichenfolge akzeptiert, und einen _resolverparameter_ , der ein **XmlNamespaceManager** -Objekt zum Auflösen von Namespaces akzeptiert. Präfixe.</span><span class="sxs-lookup"><span data-stu-id="cb469-121">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes.</span></span> <span data-ttu-id="cb469-122">Um einen einzelnen Knoten in der Hauptdatenquelle des Formulars auszuwählen, übergeben Sie einen XPath-Ausdruck, der das Feld oder die Gruppe angibt, die Sie für den _XPath_ -Parameter auswählen möchten, zusammen mit dem **XmlNamespaceManager** -Objekt, das von der [ NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) -Eigenschaft des **XmlForm** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb469-122">To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object.</span></span> <span data-ttu-id="cb469-123">Das zurückgegebene **XmlNamespaceManager**-Objekt wird mit allen Namespates, die in der Formulardefinitionsdatei (XSF) der Formularvorlage definiert sind, zum Ladezeitpunkt initialisiert.</span><span class="sxs-lookup"><span data-stu-id="cb469-123">The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="cb469-p107">Die einfachste Möglichkeit zum Erstellen eines XPath-Ausdrucks zum Auswählen eines Knotens in der Datenquelle des Formulars ist das Klicken mit der rechten Maustaste im Aufgabenbereich **Felder** auf das Feld oder die Gruppe und anschließende Klicken auf **XPath kopieren**. Fügen Sie zum Erstellen und Testen manuell bearbeiteter XPath-Ausdrücke für den Zugriff auf Knoten in einem komplexen oder überaus geschachtelten XML-Schema dem Formular ein Steuerelement vom Typ **Ausdrucksfeld** hinzu. Geben Sie dann den XPath-Ausdruck für das Steuerelement an, und zeigen Sie anschließend eine Vorschau des Formulars an, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb469-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="cb469-126">Im folgenden Beispiel wird die **SelectSingleNode** -Methode verwendet, um den einzelnen Knoten `EmailAlias` für das Feld auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cb469-126">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field.</span></span> <span data-ttu-id="cb469-127">Anschließend wird die **SetValue** -Methode der **XPathNavigator** -Klasse und die [username](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwendet, um den Wert des Felds auf den Alias des aktuellen Benutzers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cb469-127">Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
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

<span data-ttu-id="cb469-128">Weitere Informationen zum Erstellen von XPath-Ausdrücken finden Sie in der XPath-Referenz auf MSDN und in der [XML Path Language (XPath) Version 1,0 W3C Recommendation](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="cb469-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="cb469-129">Festlegen des Werts eines Knotens mit dem Attribut "xsi:nil"</span><span class="sxs-lookup"><span data-stu-id="cb469-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="cb469-130">Bei bestimmten Datentypen wird beim Versuch, den Wert eines leeren Felds programmgesteuert festzulegen, der Fehler "Nicht datentypbezogene Fehler bei der Schemaüberprüfung" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb469-130">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors."</span></span> <span data-ttu-id="cb469-131">NormalerWeise ist die Ursache dieses Fehlers, dass das [xsi: Nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) -Attribut auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb469-131">Typically the cause of this error is that the element has the [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**.</span></span> <span data-ttu-id="cb469-132">Wenn Sie das zugrunde liegende XML-Element des leeren Felds im Formular untersuchen, können Sie diese Einstellung erkennen.</span><span class="sxs-lookup"><span data-stu-id="cb469-132">If you examine the underlying XML element for the blank field in the form, you can see this setting.</span></span> <span data-ttu-id="cb469-133">Im XML-Fragment des folgenden leeren "Date"-Felds ist z. B. das **xsi:nil**-Attribute auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb469-133">For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="cb469-134">Wenn das **xsi: Nil** -Attribut auf **true**festgelegt ist, gibt es an, dass das Element vorhanden ist, aber keinen Wert hat, oder anders ausgedrückt, ist NULL.</span><span class="sxs-lookup"><span data-stu-id="cb469-134">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null .</span></span> <span data-ttu-id="cb469-135">Wenn Sie versuchen, den Wert eines solchen Knotens programmgesteuert festzulegen, zeigt InfoPath die Meldung "Schema Validierung gefundener nicht-Datentypfehler" an, da das Element derzeit als NULL gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="cb469-135">If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null .</span></span> <span data-ttu-id="cb469-136">InfoPath legt das **xsi:nil**-Attribut für null-Felder der folgenden Datentypen auf **true** fest:</span><span class="sxs-lookup"><span data-stu-id="cb469-136">InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="cb469-137">**Ganze Zahl (Ganzzahl)**</span><span class="sxs-lookup"><span data-stu-id="cb469-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="cb469-138">**Dezimal (Double)**</span><span class="sxs-lookup"><span data-stu-id="cb469-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="cb469-139">**Datum (Datum)**</span><span class="sxs-lookup"><span data-stu-id="cb469-139">**Date (date)**</span></span>
    
- <span data-ttu-id="cb469-140">**Zeit (Zeit)**</span><span class="sxs-lookup"><span data-stu-id="cb469-140">**Time (time)**</span></span>
    
- <span data-ttu-id="cb469-141">**Datum und Uhrzeit (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="cb469-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="cb469-142">Zum Vermeiden dieses Fehlers muss Ihr Code prüfen, ob das **xsi:nil**-Attribut vorhanden ist, und falls ja, es entfernen, bevor der Wert des Knotens festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cb469-142">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node.</span></span> <span data-ttu-id="cb469-143">Die folgende Unterroutine verwendet ein **XpathNavigator**-Objekt am Knoten, den Sie festlegen möchten, sucht nach dem **nil**-Attribut und löscht es, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cb469-143">The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
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

<span data-ttu-id="cb469-144">Sie können diese Unterroutine aufrufen, bevor Sie versuchen, ein Feld eines Datentyps festzulegen, das ggf. das **xsi:nil**-Attribut aufweist (siehe das folgende Beispiel, das ein "Date"-Feld festlegt).</span><span class="sxs-lookup"><span data-stu-id="cb469-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
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
> <span data-ttu-id="cb469-145">Obwohl die Implementierung des **XPathNavigator** -Objekts in InfoPath die settypisiertvalue-Methode verfügbar macht, die zum Festlegen eines Knotens mit einem Wert eines bestimmten Typs verwendet wird, wird diese Methode von InfoPath nicht implementiert. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cb469-145">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method.</span></span> <span data-ttu-id="cb469-146">Sie müssen stattdessen die **SetValue**-Methode verwenden und einen Zeichenfolgenwert im ordnungsgemäßen Format für den Datentyp des Knotens übergeben.</span><span class="sxs-lookup"><span data-stu-id="cb469-146">You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="cb469-147">Auswählen und Festlegen eines Satzes wiederholter Knoten</span><span class="sxs-lookup"><span data-stu-id="cb469-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="cb469-148">Verwenden **Sie die SELECT** -Methode der **XPathNavigator** -Klasse, um einen Satz wiederholter Felder oder Gruppen anzugeben, die eine unbestimmte Zahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb469-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="cb469-149">Diese Methode gibt ein XPathNodeIterator-Objekt zurück, das Sie zum Durchlaufen der angegebenen Auflistung von Knoten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cb469-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="cb469-150">Im folgenden Beispiel wird davon ausgegangen, dass \*\*\*\* die Formularvorlage eine Aufzählung oder ein ähnliches Steuerelement enthält, das an `field1`ein wiederholtes Element mit dem Namen gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="cb469-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="cb469-151">Der XPath des Felds wird an die **Select** -Methode übergeben, und der zurückgegebene **XPathNodeIterator** wird `nodes` der Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cb469-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="cb469-152">Sie verwenden die MoveNext-Methode, um die Auflistung von Knoten zu durchlaufen, und die Current-Eigenschaft, um ein **XPathNavigator** -Objekt zurückzugeben, das auf dem aktuellen Knoten positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="cb469-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="cb469-153">Verwenden Sie schließlich die **value** -Eigenschaft, um den Wert der einzelnen wiederholenden Felder abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb469-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
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

<span data-ttu-id="cb469-p115">Das vorherige Beispiel funktioniert mit Zeichenfolgenwerten im angegebenen wiederholten Feld. Wenn das Feld jedoch numerische Werte enthält, können Sie ähnlichen Code verwenden, um die Werte im Feld für Berechnungen, z. B. der Summe der Werte oder ihres Durchschnitts, zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="cb469-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="cb469-156">Anstatt die **Value**-Eigenschaft zum Abrufen des Werts jeder Instanz des wiederholten Felds zu verwenden, können Sie auch mithilfe der**SetValue**-Methode die Felder durchlaufen und ihre Werte festlegen (siehe das folgende Beispiel).</span><span class="sxs-lookup"><span data-stu-id="cb469-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="cb469-157">Verwenden der "XPathNavigator"-Klasse für den Zugriff auf eine externe Datenquelle</span><span class="sxs-lookup"><span data-stu-id="cb469-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="cb469-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="cb469-158"></span></span>

<span data-ttu-id="cb469-159">Um auf eine externe Datenquelle zuzugreifen, die dem Formular zugeordnet ist, geben Sie den Namen der [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) Datenquelle an die DataSources-Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse an.</span><span class="sxs-lookup"><span data-stu-id="cb469-159">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="cb469-160">Klicken Sie zum Herstellen einer Verbindung mit einer neuen externen Datenquelle oder zum Anzeigen einer Liste der Namen der vorhandenen Verbindungen mit externen Datenquellen im Menüband auf der Registerkarte **Daten** auf **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="cb469-160">To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="cb469-161">Im folgenden Codebeispiel wird gezeigt, wie ein **XPathNavigator**-Objekt am Stamm einer externen Datenquelle mit dem Namen "CityList" mithilfe der **CreateNavigator**-Methode erstellt wird und dann die **OuterXml**-Eigenschaft der **XPathNavigator**-Klasse verwendet wird, um den zurückgegebenen XML-Code in einem Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb469-161">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> <span data-ttu-id="cb469-162">Dieses Codebeispiel geht davon aus, dass Sie eine Datenverbindung mit einer Liste von Ortsnamen erstellt haben, die in einer externen Datenquelle gespeichert sind, z. B. in einem XML-Dokument oder einer SharePoint-Liste, und die Datenverbindung "CityList" genannt haben.</span><span class="sxs-lookup"><span data-stu-id="cb469-162">This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
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

<span data-ttu-id="cb469-163">Wenn Sie Zugriff auf ein **XPathNavigator**-Objekt am Stamm der externen Datenquelle erhalten haben, können Sie mithilfe von Members der **XPathNavigator**-Klasse wie den Methoden **SelectSingleNode** und **SetValue** mit den enthaltenen Daten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb469-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="cb469-164">InfoPath-Objektmodellmember, von denen die Klassen "XPathNavigator" und "XPathNodeIterator" verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cb469-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="cb469-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="cb469-165"></span></span>

<span data-ttu-id="cb469-166">Die folgende Tabelle enthält eine Übersicht aller Member des **Microsoft.Office.InfoPath**-Namespace, von denen die **XPathNavigator**-Klasse verwendet wird, um auf XML-Daten zuzugreifen, sie zu bearbeiten oder zu senden.</span><span class="sxs-lookup"><span data-stu-id="cb469-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="cb469-167">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="cb469-167">**Parent Class**</span></span>|<span data-ttu-id="cb469-168">**Member**</span><span class="sxs-lookup"><span data-stu-id="cb469-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb469-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="cb469-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="cb469-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb469-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="cb469-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb469-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="cb469-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-177">DataSource</span><span class="sxs-lookup"><span data-stu-id="cb469-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="cb469-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="cb469-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="cb469-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="cb469-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="cb469-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="cb469-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-187">FormError</span><span class="sxs-lookup"><span data-stu-id="cb469-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="cb469-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="cb469-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="cb469-190">[Hinzufügen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) von Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="cb469-191">Form Template</span><span class="sxs-lookup"><span data-stu-id="cb469-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="cb469-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb469-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="cb469-194">[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="cb469-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-197">Signatur</span><span class="sxs-lookup"><span data-stu-id="cb469-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="cb469-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="cb469-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="cb469-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-201">View</span><span class="sxs-lookup"><span data-stu-id="cb469-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="cb469-202">[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) GetContextNodes-Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="cb469-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="cb469-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="cb469-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cb469-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="cb469-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="cb469-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb469-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="cb469-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="cb469-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb469-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="cb469-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="cb469-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="cb469-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft, die ein **DataSource** -Objekt zurückgibt, das \*\*\*\* wiederum die CreateNavigator-Methode zum Erstellen eines **XPathNavigator** -Objekts bereitstellt, das sich am Stamm des dem Formular zugrunde liegenden XML-Dokuments befindet (Hauptdaten Source).</span><span class="sxs-lookup"><span data-stu-id="cb469-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="cb469-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="cb469-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="cb469-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="cb469-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb469-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="cb469-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) -Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="cb469-218">Neben den InfoPath-Objektmodellmembern, die ein **XPathNavigator**-Objekt zurückgeben oder annehmen, geben die folgenden Methoden eine Instanz der **XPathNodeIterator**-Klasse des **System.Xml.XPath**-Namespace zum Durchlaufen der XML-Knoten von Elementen zurück, die in einer Ansicht angegeben oder ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="cb469-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="cb469-219">**Übergeordnete Klasse**</span><span class="sxs-lookup"><span data-stu-id="cb469-219">**Parent Class**</span></span>|<span data-ttu-id="cb469-220">**Member**</span><span class="sxs-lookup"><span data-stu-id="cb469-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb469-221">View</span><span class="sxs-lookup"><span data-stu-id="cb469-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="cb469-222">[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) GetContextNodes-Methoden</span><span class="sxs-lookup"><span data-stu-id="cb469-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="cb469-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="cb469-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="cb469-224">Verwenden der Klassen "XPathNavigator" und "XPathNodeIterator" für in einer Ansicht ausgewählte Daten</span><span class="sxs-lookup"><span data-stu-id="cb469-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="cb469-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="cb469-225"></span></span>

<span data-ttu-id="cb469-226">Im folgenden Beispiel werden Member der Klassen **XPathNavigator** und **XPathNodeIterator** für Formulardaten in der folgenden Reihenfolge verwendet:</span><span class="sxs-lookup"><span data-stu-id="cb469-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="cb469-227">Die **CreateNavigator** -Methode der **DataSource** -Klasse wird verwendet, um eine **XPathNavigator** -Objektvariable mit dem Namen repeatingTableRow1 zu erstellen, die standardmäßig am Stamm des zugrunde liegenden XML-Dokuments des Formulars positioniert ist (die Hauptdaten Source).</span><span class="sxs-lookup"><span data-stu-id="cb469-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="cb469-228">Die **SelectSingleNode** -Methode der **XPathNavigator** -Klasse wird verwendet, um die Position des **XPathNavigator** -Objekts in die erste Zeile eines **wiederholten Table** -Steuerelements zu verschieben, das an group2 in der Datenquelle gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="cb469-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="cb469-229">Die repeatingTableRow1-Objektvariable wird an die **SelectNodes**-Methode der **View**-Klasse übergeben, um die Knoten in dieser Zeile auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cb469-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="cb469-230">Eine **XPathNodeIterator** -Objektvariable mit dem Namen selectedNodes wird deklariert, und die **GetSelectedNodes** -Methode der **View** -Klasse wird verwendet, um das **XPathNodeIterator** -Objekt mit den ausgewählten Knoten aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="cb469-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="cb469-231">Die **count** -Eigenschaft der **XPathNodeIterator** -Klasse wird verwendet, um die Anzahl der in der selectedNodes-Objektvariablen enthaltenen Knoten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb469-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="cb469-232">Eine For/Each-Schleife dient zum Durchlaufen der Knoten in der selectedNodes-Objektvariablen und zum Anzeigen von Informationen zu den einzelnen Knoten mithilfe der Eigenschaften **Name**, **InnerXml** und **Value** der **XPathNavigator**-Klasse.</span><span class="sxs-lookup"><span data-stu-id="cb469-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
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

<span data-ttu-id="cb469-233">Weitere Informationen zum Arbeiten mit XML-Daten aus InfoPath-Formularvorlagen finden Sie unter Arbeiten mit XML-Daten mithilfe der XPathNavigator-Klasse in InfoPath 2007-Formularvorlagen.</span><span class="sxs-lookup"><span data-stu-id="cb469-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

