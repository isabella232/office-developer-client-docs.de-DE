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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437399"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell

Formularvorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten, verwenden Microsoft XML Core Services (MSXML) intern für XML. Bei verwaltetem Code ist es häufig einfacher, die vom **System.Xml**-Namespace bereitgestellte XML-Unterstützung in der .NET Framework-Bibliothek zu verwenden. Es ist für MSXML und **System.Xml** kein systemeigener Objektaustausch möglich, sodass die XML-Daten jedes Mal konvertiert werden müssen, wenn XML-Daten an InfoPath und anderen verwalteten Code übergeben werden sollen. Sie können XML-Daten von **System.Xml**-Objekten mit InfoPath-Formularcode austauschen, indem Sie die in diesem Thema beschriebenen Techniken verwenden. 
  
Wenn Sie Member des Namespace **System. XML** in einem Projekt mit verwaltetem Code verwenden möchten, das das InfoPath 2003-Objektmodell verwendet, müssen Sie auf der Registerkarte **.net** des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 einen Verweis auf **System. XML** hinzufügen. 
  
 **Hinweise**
  
- Informationen zu MSXML finden Sie im MSXML SDK.
    
- Elemente des MSXML-Objektmodells, die vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace umschlossen werden, können Delegaten im Formularcode von Formularvorlagen mit verwaltetem Code nicht zugewiesen werden. 
    
- Wenn Sie den Code Ihrer Formularvorlage aktualisieren, um das von Mitgliedern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell zu verwenden, wird **System. XML** nativ verwendet. Sie müssen in diesem Fall jedoch den kompletten Code konvertieren, um das neue Objektmodell verwenden zu können. Klicken Sie zum Konvertieren der Formularvorlage zum Verwenden des neuen Objektmodells im Dialogfeld **Formularoptionen** in der Kategorie **Programmierung** auf **OM aktualisieren**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml

Im folgenden Codebeispiel wird veranschaulicht, wie ein vollständiges XML-DOM aus dem **System. XML** -Code mithilfe der InfoPath-Methode [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) und den Mitgliedern von Microsoft XML Core Services geladen wird, die von Mitgliedern [des Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace. 
  
Bei den folgenden Beispielen ist eine **using**- oder **Imports**-Direktive für **System.Xml** im Deklarationsabschnitt des Formularcodemoduls erforderlich. Da die **Last** -Methode der XmlDocument **** -Klasse **System. Security. Permissions. FileIOPermission**erfordert, müssen Sie zusätzlich die Sicherheitsstufe der Formularvorlage als **voll vertrauenswürdig** konfigurieren, indem Sie die Sicherheitseinstellungen verwenden. ** und Vertrauens** Kategorie des Dialogfelds **Formularoptionen** . 
  
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


