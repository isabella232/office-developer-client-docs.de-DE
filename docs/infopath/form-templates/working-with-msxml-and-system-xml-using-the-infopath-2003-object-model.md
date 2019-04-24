---
title: Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen mit MSXML5, MSXML5 [InfoPath 2007], MSXML5-Skript [InfoPath 2007], InfoPath 2007, verwenden von MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom System.Xml-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und System.Xml kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von System.Xml-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299720"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="bf5e9-107">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="bf5e9-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="bf5e9-108">Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-108">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML.</span></span> <span data-ttu-id="bf5e9-109">Bei verwaltetem Code ist es häufig einfacher, die vom **System.Xml**-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-109">In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library.</span></span> <span data-ttu-id="bf5e9-110">Es ist für MSXML und **System.Xml** kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-110">MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted.</span></span> <span data-ttu-id="bf5e9-111">Sie können XML-Daten von **System.Xml**-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-111">You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="bf5e9-112">Wenn Sie Member des Namespace **System. XML** in einem Projekt mit verwaltetem Code verwenden möchten, das das InfoPath 2003-Objektmodell verwendet, müssen Sie auf der Registerkarte **.net** des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 einen Verweis auf **System. XML** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="bf5e9-113">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="bf5e9-113">**Notes**</span></span>
  
- <span data-ttu-id="bf5e9-114">Informationen zu MSXML finden Sie im MSXML SDK.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="bf5e9-115">Elemente des MSXML-Objektmodells, die vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace umschlossen werden, können Delegaten im Formularcode von Formularvorlagen mit verwaltetem Code nicht zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="bf5e9-116">Wenn Sie den Code Ihrer Formularvorlage aktualisieren, um das von Mitgliedern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell zu verwenden, wird **System. XML** nativ verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-116">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively.</span></span> <span data-ttu-id="bf5e9-117">Sie müssen in diesem Fall jedoch den kompletten Code konvertieren, um das neue Objektmodell verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-117">However, when doing so, you must manually convert all of your code to use the new object model.</span></span> <span data-ttu-id="bf5e9-118">Klicken Sie zum Konvertieren der Formularvorlage zum Verwenden des neuen Objektmodells im Dialogfeld **Formularoptionen** in der Kategorie **Programmierung** auf **OM aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-118">To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="bf5e9-119">Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="bf5e9-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="bf5e9-120">Im folgenden Codebeispiel wird veranschaulicht, wie ein vollständiges XML-DOM aus dem **System. XML** -Code mithilfe der InfoPath-Methode [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) und den Mitgliedern von Microsoft XML Core Services geladen wird, die von Mitgliedern [des Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="bf5e9-121">Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-121">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> <span data-ttu-id="bf5e9-122">Da die **Last** -Methode der XmlDocument \*\*\*\* -Klasse **System. Security. Permissions. FileIOPermission**erfordert, müssen Sie zusätzlich die Sicherheitsstufe der Formularvorlage als **voll vertrauenswürdig** konfigurieren, indem Sie die Sicherheitseinstellungen verwenden. \*\* und Vertrauens\*\* Kategorie des Dialogfelds **Formularoptionen** .</span><span class="sxs-lookup"><span data-stu-id="bf5e9-122">Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
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

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="bf5e9-123">Laden eines einzelnen Knotens aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="bf5e9-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="bf5e9-124">Das folgende Beispiel zeigt eine Funktion, mit der dargestellt wird, wie ein einzelner Knoten aus einem **System.Xml**.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-124">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**.</span></span> <span data-ttu-id="bf5e9-125">**XmlElement** mithilfe der eingebundenen **createNode**-Methode von MSXML geklont wird.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-125">**XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="bf5e9-126">Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf5e9-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
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


