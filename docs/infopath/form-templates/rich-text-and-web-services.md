---
title: Rich-Text und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath unterstützt das Binden eines Rich-Text-Feld-Steuerelements in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Senden von Daten aus einem Rich-Text-Feld-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss dem XHTML-Format (Extensible HyperText Markup Language) entsprechen. Beispielsweise würde das Schema für ein Element mit dem Namen MyRichTextElement, das Rich-Text enthält, die folgende XML-Schemadefinition aufweisen:'
ms.openlocfilehash: f32396d5225459b3a1b31506f9246407bc27468c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580503"
---
# <a name="rich-text-and-web-services"></a>Rich-Text und Webdienste

Microsoft InfoPath unterstützt das Binden eines **Rich-Text-Feld-Steuerelements** in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Senden von Daten aus einem Rich-Text-Feld-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss dem XHTML-Format (Extensible HyperText Markup Language) entsprechen. Beispielsweise würde das Schema für ein Element mit dem  `MyRichTextElement` Namen, das Rich-Text enthält, die folgende XML-Schemadefinition aufweisen: 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

Bevor ein **Feld für Rich-Text**-Steuerelement an das XHTML-Element gebunden werden kann, muss das Element mit einem Wrapperknoten gepackt werden; dieser Wrapperknoten kann zu einem beliebigen Namespace gehören. Der Wrapperknoten kann so aussehen: 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

In diesem Thema wird das Erstellen eines Webdiensts beschrieben, der XHTML senden und empfangen kann, und wie InfoPath zum Binden an die Webdienstparameter verwendet wird. In diesem Thema finden Sie keine ausführlichen Anweisungen zum Erstellen eines solchen Webdiensts. Es wird davon ausgegangen, dass Sie bereits mit der Arbeit mit Webdiensten vertraut sind.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML

Der Beispielwebdienst speichert die XHTML-Daten, die er sendet und empfängt, in einer XML-Datei auf dem Server. Diese Datei mit dem Namen out.xml dient als Datenquelle, in der die XHTML-Daten gespeichert werden. Es gibt zwei Webmethoden, die verfügbar gemacht werden, damit eine Clientanwendung eine Schnittstelle mit der XHTML-Datenquelle herstellen kann:  `getXhtml` und  `setXhtml` . Die  `getXhtml` Webdienstmethode gibt einen **XmlNode-Wert** zurück, der den XHTML-Code enthält, der an ein InfoPath-Rich-Text-Feldsteuerelement gebunden werden kann. Die  `setXhtml` Webdienstmethode akzeptiert **xmlNode** als die Daten, die in der out.xml-Datei gespeichert werden sollen. 
  
> [!NOTE]
> Diese Webmethoden erfordern **die Verwendung von** Anweisungen, die auf die **System.IO** und **System.Xml** Namespaces verweisen. 
  
Die `getXhtml` Webdienstmethode versucht, die XML-Daten zu laden, die aus der out.xml-Datei im Datenordner auf Laufwerk C zurückgegeben werden sollen. Wenn ein Fehler auftritt, weil die Datei nicht gefunden wird oder keinen  gültigen XML-Code enthält, gibt die Methode ein leeres DIV-HTML-Element zurück, das auf den XHTML-Namespace verweist. 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

Die  `setXhtml` Webdienstmethode akzeptiert XHTML aus einem **Rich-Text-Feld-Steuerelement** in einem InfoPath-Formular. Da Webdienste keine Knotenliste unterstützen, akzeptiert der Webdienst beim Senden eines Rich-Text-Felds mit mehreren Zeilen an einen Webdienst nur die erste Zeile und ignoriert den Rest. 
  
Die  `setXhtml` Beispielmethode geht davon aus, dass sie einen XML-Knoten auf oberster Ebene empfängt, der in den meisten Fällen in ein **DIV-Element** eingeschlossen wird. Wenn der empfangene XML-Code kein Umbruchelement enthält, z. B. wenn Text innerhalb des **Rich-Text-Feld-Steuerelements** keine Formatierung aufweist, erkennt diese Methode dies, indem überprüft wird, ob die **NodeType-Eigenschaft** angibt, dass es sich bei der übergebenen XML um einen Textknoten handelt. Wenn es sich bei dem XML-Code um einen Textknoten handelt, erstellt die Methode ein **DIV-Element** und kopiert den Textknoteninhalt in das DIV-Element, **sodass** div einen untergeordneten Textknoten mit dem Text enthält, der an den Webdienst gesendet wurde.  Der von dieser Methode empfangene XML-Code wird in die out.xml-Datei im Datenordner auf laufwerk C geschrieben. 
  
> [!NOTE]
> Die  `setXhtml` Beispielmethode wurde geschrieben, um XHTML-Daten jeder Größe zu akzeptieren. In der Praxis sollten Sie immer überprüfen, wie viele Daten übertragen werden und eine Höchstgrenze für die Menge der übertragenen Daten festlegen. 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Erstellen eines InfoPath-Formulars zum Austauschen von Daten mit dem Beispielwebdienst

Führen Sie die folgenden Schritte aus, um ein Formular zum Testen des Beispielwebdiensts zu erstellen.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>So erstellen Sie ein Formular, über das eine Verbindung mit dem Beispielwebdienst hergestellt wird

1. Öffnen Sie den InfoPath-Formular-Designer.
    
2. Doppelklicken Sie auf der Registerkarte **Neu** unter **Erweiterte Formularvorlagen** auf **Webdienst**.
    
3. Wählen Sie im Dialogfeld **Datenverbindungs-Assistent** die Option **Daten empfangen** aus, und klicken Sie dann auf **Weiter**.
    
4. Geben Sie die Adresse des Webdiensts ein, der die Beispiele für Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.  
    
5. Wählen Sie **getXhtml** als Vorgang für die Empfangsmethode aus, und klicken Sie dann auf **Weiter**.
    
6. Für die **getXHTML**-Webdienstmethode können keine Parameter verwendet werden. Klicken Sie daher auf **Weiter**.
    
7. Klicken Sie auf **Fertig stellen**.
    
8. Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Übermittlungsaktionen** auf **An andere Speicherorte** und dann auf **Webdienst**, um zum Senden der Daten den gleichen Webdienst zu verwenden. 
    
9. Geben Sie die Adresse des Webdiensts ein, der die Beispiele für Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.
    
10. Wählen Sie **setXhtml** als Vorgang für die Sendemethode aus, und klicken Sie dann auf **Weiter**.
    
11. Klicken Sie auf **"Ändern",** erweitern Sie den Ordner **"dataFields",** erweitern Sie den Ordner **"s0:getXhtmlResponse",** erweitern Sie den Ordner **"getXhtmlResult",** wählen Sie das **Element "MyRichTextElement"** aus, und klicken Sie dann auf **"Weiter".**
    
12. Klicken Sie auf **Fertig stellen**.
    
13. Erweitern Sie im Aufgabenbereich **Felder** den Ordner **dataFields**. 
    
14. Erweitern Sie die Ordner **s0:getXhtmlResponse** und **getXhtmlResult**, und ziehen Sie dann das **MyRichTextElement**-Element auf das Formular. InfoPath erkennt, dass das **MyRichTextElement-Element** ein XHTML-Element ist, und verwendet ein Rich-Text-Feld-Steuerelement, um eine Bindung daran zu erstellen. 
    
15. Speichern oder veröffentlichen Sie das Formular.
    
Um das Formular zu testen, öffnen Sie das Formular, und geben Sie Rich-Text-Inhalte wie Bilder, Tabellen und formatierten Text ein. Klicken Sie auf dem Menüband auf **"Übermitteln",** um den Rich-Text-Inhalt in der out.xml-Datei auf dem Server zu speichern. Klicken Sie  auf der Registerkarte Ansicht auf Abfrage und anschließend auf die Schaltfläche Abfrage **ausführen** im Formular.  Das **Rich-Text-Feld-Steuerelement** sollte den XHTML-Inhalt aus der out.xml Datei anzeigen. Wenn das Rich-Text-Feld mehrere Zeilen enthält, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest. 
  

