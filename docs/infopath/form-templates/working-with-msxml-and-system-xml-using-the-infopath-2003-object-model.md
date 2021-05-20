---
title: Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen mit msxml5,MSXML5 [InfoPath 2007],MSXML5-Skript [InfoPath 2007],InfoPath 2007 mit MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom System.Xml-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und System.Xml kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von System.Xml-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437399"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="10d30-107">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="10d30-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="10d30-p102">Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom **System.Xml**-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und **System.Xml** kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von **System.Xml**-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden.</span><span class="sxs-lookup"><span data-stu-id="10d30-p102">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML. In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library. MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted. You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="10d30-112">Um Elemente des **System.Xml-Namespace** in einem verwalteten Codeprojekt zu verwenden, das das InfoPath 2003-Objektmodell verwendet,  müssen Sie auf der Registerkarte **.NET** des Dialogfelds Verweis hinzufügen in Visual Studio 2012 einen Verweis auf **System.Xml** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="10d30-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="10d30-113">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="10d30-113">**Notes**</span></span>
  
- <span data-ttu-id="10d30-114">Referenzinformationen zu MSXML finden Sie im MSXML SDK.</span><span class="sxs-lookup"><span data-stu-id="10d30-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="10d30-115">Member des MSXML-Objektmodells, die vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) umschlossen werden, können Stellvertretungen im Formularcode von Formularvorlagen mit verwalteten Code nicht zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="10d30-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="10d30-116">Wenn Sie den Code Ihrer Formularvorlage so aktualisieren, dass das objektmodell verwendet wird, das von Mitgliedern der [Microsoft.Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** wird nativ verwendet.</span><span class="sxs-lookup"><span data-stu-id="10d30-116">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively.</span></span> <span data-ttu-id="10d30-117">Sie müssen in diesem Fall jedoch den kompletten Code konvertieren, um das neue Objektmodell verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="10d30-117">However, when doing so, you must manually convert all of your code to use the new object model.</span></span> <span data-ttu-id="10d30-118">Klicken Sie zum Konvertieren der Formularvorlage zum Verwenden des neuen Objektmodells im Dialogfeld **Formularoptionen** in der Kategorie **Programmierung** auf **OM aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="10d30-118">To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="10d30-119">Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="10d30-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="10d30-120">Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein gesamtes XML-DOM aus **System.Xml-Code** mit der InfoPath [CreateDOM-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) und den Mitgliedern von Microsoft XML Core Services laden, die von Mitgliedern des [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespaces](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="10d30-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="10d30-p104">Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich. Da die **Load**-Methode der **XmlDocument**-Klasse **System.Security.Permissions.FileIOPermission** erfordert, müssen Sie darüber hinaus die Sicherheitsebene der Formularvorlage als **Voll vertrauenswürdig** konfigurieren. Verwenden Sie hierzu im Dialogfeld **Formularoptionen** die Kategorie **Sicherheit und Vertrauensstellung**.</span><span class="sxs-lookup"><span data-stu-id="10d30-p104">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module. Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="10d30-123">Laden eines einzelnen Knotens aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="10d30-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="10d30-124">Das folgende Beispiel zeigt eine Funktion, mit der dargestellt wird, wie ein einzelner Knoten aus einem **System.Xml**.</span><span class="sxs-lookup"><span data-stu-id="10d30-124">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**.</span></span> <span data-ttu-id="10d30-125">**XmlElement** mithilfe der eingebundenen **createNode**-Methode von MSXML geklont wird.</span><span class="sxs-lookup"><span data-stu-id="10d30-125">**XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="10d30-126">Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="10d30-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


