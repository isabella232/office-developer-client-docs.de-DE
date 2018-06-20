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
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell

Formular Vorlagenprojekte, die mit dem InfoPath 2003-Objektmodell arbeiten verwenden Microsoft XML Core Services (MSXML) intern XML entwickelt. In verwaltetem Code ist es oft einfacher mithilfe die XML-Unterstützung durch den **System.Xml** -Namespace in der .NET Framework-Klassenbibliothek. MSXML und **System.Xml** kann nicht Objekte systemintern unterstützt, exchange, wenn Sie XML-Daten zwischen InfoPath und anderen verwalteten Code übergeben möchten, muss die XML-Daten, konvertiert werden soll. Sie können die XML-Daten aus **System.Xml** -Objekte mit InfoPath-Formularcode austauschen, mithilfe der Verfahren in diesem Thema. 
  
Um die Mitglieder der **System.Xml** -Namespace in ein Projekt mit verwaltetem Code verwenden zu können, die das InfoPath 2003-Objektmodell verwendet, müssen Sie einen Verweis auf **"System.xml"** auf der Registerkarte **.NET** des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 hinzufügen. 
  
 **Anmerkungen**
  
- Referenzinformationen zu MSXML finden Sie unter MSXML SDK.
    
- Member des MSXML-Objektmodells, die vom [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace eingebunden sind können nicht Delegaten im Formularcode von Formularvorlagen mit verwaltetem Code zugewiesen werden. 
    
- Wenn Sie den Code der Formularvorlage, verwenden Sie die Member des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte Objektmodell aktualisieren, wird eine systemeigene **System.Xml** verwendet. Allerdings müssen dabei Sie manuell alle des Codes mit dem neuen Objektmodell konvertieren. Klicken Sie auf **OM aktualisieren**, um die Formularvorlage so verwenden Sie das neue Objektmodell in der Kategorie **Programmierung** im Dialogfeld **Formularoptionen** zu konvertieren.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Laden eines vollständigen XML-DOMs (Document Object Model) aus System.Xml

Im folgenden Codebeispiel veranschaulicht, wie eine gesamte XML-DOM aus **System.Xml** -Code mithilfe der InfoPath- [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) -Methode und die Mitglieder von Microsoft XML Core Services, die durch ein Mitglied der [eingebunden sind laden Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) Namespace. 
  
In den folgenden Beispielen ist eine **Using-** oder **Imports** -Direktive für **System.Xml** im Deklarationsabschnitt des formularcodemoduls erforderlich. Darüber hinaus, da die **Load** -Methode der **XmlDocument** -Klasse **System.Security.Permissions.FileIOPermission**erfordert, müssen Sie die Sicherheitsstufe der Formularvorlage als **Voll vertrauenswürdig** mithilfe der **Sicherheit konfigurieren und Vertrauensstellung** Kategorie im Dialogfeld **Formularoptionen** . 
  
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

Das folgende Codebeispiel zeigt eine Funktion, die einen einzelnen Knoten aus einer **System.Xml**Klonen veranschaulicht. **XmlElement** mithilfe der eingebundenen **CreateNode** -Methode für die MSXML. 
  
In den folgenden Beispielen ist eine **Using-** oder **Imports** -Direktive für **System.Xml** im Deklarationsabschnitt des formularcodemoduls erforderlich. 
  
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


