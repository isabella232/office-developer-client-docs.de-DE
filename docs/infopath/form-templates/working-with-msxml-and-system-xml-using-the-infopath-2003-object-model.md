---
title: Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, mit msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
ms.localizationpriority: medium
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom System.Xml-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und System.Xml kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von System.Xml-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden.
ms.openlocfilehash: 7fa559974a542aeb3472f6ef51ac6869a94cf6d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588371"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell

Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom **System.Xml**-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und **System.Xml** kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von **System.Xml**-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden. 
  
Um Member des **System.Xml-Namespace** in einem Projekt mit verwaltetem Code zu verwenden, das das InfoPath 2003-Objektmodell verwendet, müssen Sie einen Verweis auf **System.Xml** auf der Registerkarte **.NET** des Dialogfelds **"Verweis hinzufügen"** in Visual Studio 2012 hinzufügen. 
  
 **Hinweise**
  
- Informationen zum Anzeigen von Referenzinformationen zu MSXML finden Sie im MSXML SDK.
    
- Elemente des MSXML-Objektmodells, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) umschlossen wird, können Stellvertretungen im Formularcode von Formularvorlagen mit verwaltetem Code nicht zugewiesen werden. 
    
- Wenn Sie den Code Ihrer Formularvorlage so aktualisieren, dass er das von Mitgliedern der Microsoft.Office bereitgestellte Objektmodell [verwendet. InfoPath-Namespace,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) **System.Xml** wird nativ verwendet. Sie müssen in diesem Fall jedoch den kompletten Code konvertieren, um das neue Objektmodell verwenden zu können. Klicken Sie zum Konvertieren der Formularvorlage zum Verwenden des neuen Objektmodells im Dialogfeld **Formularoptionen** in der Kategorie **Programmierung** auf **OM aktualisieren**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml

Im folgenden Codebeispiel wird veranschaulicht, wie ein gesamtes XML-DOM aus **System.Xml** Code mithilfe der InfoPath [CreateDOM-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) und der Member von Microsoft XML Core Services geladen wird, die von Mitgliedern des [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) umbrochen werden. 
  
Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich. Da die **Load**-Methode der **XmlDocument**-Klasse **System.Security.Permissions.FileIOPermission** erfordert, müssen Sie darüber hinaus die Sicherheitsebene der Formularvorlage als **Voll vertrauenswürdig** konfigurieren. Verwenden Sie hierzu im Dialogfeld **Formularoptionen** die Kategorie **Sicherheit und Vertrauensstellung**. 
  
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

## <a name="loading-a-single-node-from-systemxml"></a>Laden eines einzelnen Knotens aus System.Xml

Das folgende Beispiel zeigt eine Funktion, mit der dargestellt wird, wie ein einzelner Knoten aus einem **System.Xml**. **XmlElement** mithilfe der eingebundenen **createNode**-Methode von MSXML geklont wird. 
  
Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich. 
  
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


