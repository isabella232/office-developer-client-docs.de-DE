---
title: Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, mit msxml5 MSXML5 [InfoPath 2007] MSXML5-Skript [InfoPath 2007], InfoPath 2007 mithilfe von MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Formular Vorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten verwenden Microsoft XML Core Services (MSXML) intern XML entwickelt. In verwaltetem Code ist es oft einfacher mithilfe die XML-Unterstützung durch den System.Xml-Namespace in der .NET Framework-Klassenbibliothek. MSXML und System.Xml kann nicht Objekte systemintern unterstützt, exchange, wenn Sie XML-Daten zwischen InfoPath und anderen verwalteten Code übergeben möchten, muss die XML-Daten, konvertiert werden soll. Sie können die XML-Daten aus System.Xml-Objekte mit InfoPath-Formularcode austauschen, mithilfe der Verfahren in diesem Thema.
ms.openlocfilehash: 345aeb3dcb6e9621657bd2b21f98c87cb5e61993
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790843"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="b66d2-107">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="b66d2-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="b66d2-108">Formular Vorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten verwenden Microsoft XML Core Services (MSXML) intern XML entwickelt.</span><span class="sxs-lookup"><span data-stu-id="b66d2-108">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML.</span></span> <span data-ttu-id="b66d2-109">In verwaltetem Code ist es oft einfacher mithilfe die XML-Unterstützung durch den **System.Xml** -Namespace in der .NET Framework-Klassenbibliothek.</span><span class="sxs-lookup"><span data-stu-id="b66d2-109">In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library.</span></span> <span data-ttu-id="b66d2-110">MSXML und **System.Xml** kann nicht Objekte systemintern unterstützt, exchange, wenn Sie XML-Daten zwischen InfoPath und anderen verwalteten Code übergeben möchten, muss die XML-Daten, konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b66d2-110">MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted.</span></span> <span data-ttu-id="b66d2-111">Sie können die XML-Daten aus **System.Xml** -Objekte mit InfoPath-Formularcode austauschen, mithilfe der Verfahren in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b66d2-111">You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="b66d2-112">Um die Mitglieder der **System.Xml** -Namespace in ein Projekt mit verwaltetem Code verwenden zu können, die das InfoPath 2003-Objektmodell verwendet, müssen Sie einen Verweis auf **"System.xml"** auf der Registerkarte **.NET** des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b66d2-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="b66d2-113">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="b66d2-113">**Notes**</span></span>
  
- <span data-ttu-id="b66d2-114">Referenzinformationen zu MSXML finden Sie unter MSXML SDK.</span><span class="sxs-lookup"><span data-stu-id="b66d2-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="b66d2-115">Member des MSXML-Objektmodells, die vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace eingebunden sind können nicht Delegaten im Formularcode von Formularvorlagen mit verwaltetem Code zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b66d2-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="b66d2-116">Wenn Sie den Code der Formularvorlage, verwenden Sie die Member des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell aktualisieren, wird eine systemeigene **System.Xml** verwendet.</span><span class="sxs-lookup"><span data-stu-id="b66d2-116">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively.</span></span> <span data-ttu-id="b66d2-117">Allerdings müssen dabei Sie manuell alle des Codes mit dem neuen Objektmodell konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b66d2-117">However, when doing so, you must manually convert all of your code to use the new object model.</span></span> <span data-ttu-id="b66d2-118">Klicken Sie auf **OM aktualisieren**, um die Formularvorlage so verwenden Sie das neue Objektmodell in der Kategorie **Programmierung** im Dialogfeld **Formularoptionen** zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b66d2-118">To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="b66d2-119">Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="b66d2-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="b66d2-120">Im folgenden Codebeispiel veranschaulicht, wie eine gesamte XML-DOM aus **System.Xml** -Code mithilfe der InfoPath- [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) -Methode und die Mitglieder von Microsoft XML Core Services, die durch ein Mitglied der [eingebunden sind laden Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) Namespace.</span><span class="sxs-lookup"><span data-stu-id="b66d2-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="b66d2-121">In den folgenden Beispielen ist eine **Using-** oder **Imports** -Direktive für **System.Xml** im Deklarationsabschnitt des formularcodemoduls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b66d2-121">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> <span data-ttu-id="b66d2-122">Darüber hinaus, da die **Load** -Methode der **XmlDocument** -Klasse **System.Security.Permissions.FileIOPermission**erfordert, müssen Sie die Sicherheitsstufe der Formularvorlage als **Voll vertrauenswürdig** mithilfe der **Sicherheit konfigurieren und Vertrauensstellung** Kategorie im Dialogfeld **Formularoptionen** .</span><span class="sxs-lookup"><span data-stu-id="b66d2-122">Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
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

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="b66d2-123">Laden eines einzelnen Knotens aus System.Xml</span><span class="sxs-lookup"><span data-stu-id="b66d2-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="b66d2-124">Das folgende Codebeispiel zeigt eine Funktion, die einen einzelnen Knoten aus einer **System.Xml**Klonen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b66d2-124">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**.</span></span> <span data-ttu-id="b66d2-125">**XmlElement** mithilfe der eingebundenen **CreateNode** -Methode für die MSXML.</span><span class="sxs-lookup"><span data-stu-id="b66d2-125">**XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="b66d2-126">In den folgenden Beispielen ist eine **Using-** oder **Imports** -Direktive für **System.Xml** im Deklarationsabschnitt des formularcodemoduls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b66d2-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
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


