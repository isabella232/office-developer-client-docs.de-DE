---
title: Rich-Text und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath unterstützt das Binden eines Rich-Text-Box-Steuerelements in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Übermitteln von Daten aus einem Rich-Text-Box-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss das Format Extensible HyperText Markup Language (XHTML) einhalten. Beispielsweise hat das Schema für ein Element mit dem Namen MyRichTextElement, das Rich Text enthält, die folgende XML-Schemadefinition:'
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299846"
---
# <a name="rich-text-and-web-services"></a>Rich-Text und Webdienste

Microsoft InfoPath unterstützt das Binden eines **Rich-Text-Box-Steuerelements** in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Übermitteln von Daten aus einem Rich-Text-Box-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss das Format Extensible HyperText Markup Language (XHTML) einhalten. Das Schema für ein Element mit dem Namen Rich Text hat beispielsweise die  `MyRichTextElement` folgende XML-Schemadefinition: 
  
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

In diesem Thema wird das Erstellen eines Webdiensts beschrieben, der XHTML senden und empfangen kann, sowie die Verwendung von InfoPath zum Binden an die Webdienstparameter. Dieses Thema enthält keine detaillierten Anweisungen zum Erstellen eines solchen Webdiensts. Es wird davon ausgegangen, dass Sie bereits mit der Arbeit mit Webdiensten vertraut sind.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML

Der Beispielwebdienst speichert die XHTML-Daten, die er sendet und empfängt, in einer XML-Datei auf dem Server. Diese Datei mit dem Namen out.xml als Datenquelle, in der die XHTML-Daten gespeichert werden. Es gibt zwei Webmethoden, die verfügbar gemacht werden, damit eine Clientanwendung eine Schnittstelle mit der XHTML-Datenquelle verwenden kann:  `getXhtml` und  `setXhtml` . Die Webdienstmethode gibt eine XmlNode zurück, die XHTML enthält, die an ein `getXhtml` InfoPath-Rich-Text-Feldsteuerelement gebunden werden kann.  Die  `setXhtml` Webdienstmethode akzeptiert ein **XmlNode-Element** als Daten, die in der Datei out.xml werden. 
  
> [!NOTE]
> Diese Webmethoden erfordern **die Verwendung von** **Anweisungen,** die auf die System.IO und **System.Xml** verweisen. 
  
Die Webdienstmethode versucht, die out.xml zu laden, die aus der #out.xml im Ordner Daten auf Laufwerk `getXhtml` C zurückgegeben werden sollen. Wenn ein Fehler auftritt, da die Datei nicht gefunden wird oder keinen  gültigen XML-Code enthält, gibt die Methode ein leeres DIV-HTML-Element zurück, das auf den XHTML-Namespace verweist. 
  
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

Die  `setXhtml` Webdienstmethode akzeptiert XHTML von einem **Rich-Text-Box-Steuerelement** in einem InfoPath-Formular. Da Webdienste keine Knotenliste unterstützen, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest, wenn ein Rich-Text-Feld mit mehreren Zeilen an einen Webdienst gesendet wird. 
  
Die Beispielmethode geht davon aus, dass sie einen XML-Knoten der obersten Ebene erhält, der in den meisten Fällen in ein  `setXhtml` **DIV-Element umschlossen** wird. Wenn die empfangene XML kein Umbruchelement enthält, z. B. wenn Text im **Rich Text Box-Steuerelement** keine Formatierung enthält, erkennt diese Methode dies, indem sie überprüft, ob die **NodeType-Eigenschaft** angibt, dass die übergebene XML ein Textknoten ist. Wenn es sich bei der XML um einen Textknoten handelt, erstellt die Methode ein **DIV-Element** und kopiert den Textknoteninhalt in das **DIV,** sodass das **DIV** einen untergeordneten Textknoten mit dem Text enthält, der an den Webdienst gesendet wurde. Die von dieser Methode empfangene XML wird in die datei out.xml im Ordner Daten auf laufwerk C geschrieben. 
  
> [!NOTE]
> Die  `setXhtml` Beispielmethode wurde so geschrieben, dass sie XHTML-Daten beliebiger Größe akzeptiert. In der Praxis sollten Sie immer überprüfen, wie viele Daten übertragen werden und eine Höchstgrenze für die Menge der übertragenen Daten festlegen. 
  
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
    
11. Klicken **Sie auf** Ändern, erweitern Sie den Ordner **dataFields,** erweitern Sie den **Ordner s0:getXhtmlResponse,** erweitern Sie den **Ordner getXhtmlResult,** wählen Sie das **MyRichTextElement-Element** aus, und klicken Sie dann auf **Weiter**.
    
12. Klicken Sie auf **Fertig stellen**.
    
13. Erweitern Sie im Aufgabenbereich **Felder** den Ordner **dataFields**. 
    
14. Erweitern Sie die Ordner **s0:getXhtmlResponse** und **getXhtmlResult**, und ziehen Sie dann das **MyRichTextElement**-Element auf das Formular. InfoPath erkennt, dass das **MyRichTextElement-Element** ein XHTML-Element ist, und verwendet ein Rich-Text-Feld-Steuerelement, um eine Bindung an das Element zu verwenden. 
    
15. Speichern oder veröffentlichen Sie das Formular.
    
Um das Formular zu testen, öffnen Sie das Formular, und geben Sie einige Rich-Text-Inhalte wie Bilder, Tabellen und formatierten Text ein. Klicken **Sie auf** dem Menüband auf Absenden, um den Rich-Text-Inhalt in der out.xml auf dem Server zu speichern. Klicken **Sie auf** der Registerkarte **Ansicht** auf Abfrage, und klicken Sie dann auf die **Schaltfläche** Abfrage ausführen im Formular. Das **Rich Text Box-Steuerelement** sollte den XHTML-Inhalt aus der out.xml anzeigen. Wenn das Rich-Text-Feld mehrere Zeilen enthält, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest. 
  

