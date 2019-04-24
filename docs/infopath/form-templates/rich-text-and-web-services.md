---
title: Rich-Text und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath unterstützt die Bindung eines Rich-Text-Feld-Steuerelements in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Senden von Daten aus einem Rich-Text-Feld-Steuerelement an ein XML-Element über einen Webdienst. Das-Element muss das Extensible HyperText Markup Language (XHTML)-Format einhalten. Beispielsweise würde das Schema für ein Element namens MyRichTextElement, das Rich-Text enthält, die folgende XML-Schema Definition aufweisen:'
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299846"
---
# <a name="rich-text-and-web-services"></a>Rich-Text und Webdienste

Microsoft InfoPath unterstützt die Bindung eines **Rich-Text-Feld** -Steuerelements in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Senden von Daten aus einem Rich-Text-Feld-Steuerelement an ein XML-Element über einen Webdienst. Das-Element muss das Extensible HyperText Markup Language (XHTML)-Format einhalten. Beispielsweise würde das Schema für ein Element namens `MyRichTextElement` , das Rich-Text enthält, die folgende XML-Schema Definition aufweisen: 
  
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

In diesem Thema wird der Vorgang des Erstellens eines Webdiensts beschrieben, der XHTML senden und empfangen kann, und die Verwendung von InfoPath zur Bindung an die Webdienstparameter. Dieses Thema enthält keine detaillierten Anweisungen zum Erstellen eines solchen Webdiensts. Es wird davon ausgegangen, dass Sie bereits über eine gewisse Vertrautheit mit Webdiensten verfügen.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML

Der Beispiel-Webdienst speichert die XHTML-Daten, die in einer XML-Datei auf dem Server gesendet und empfangen werden. Diese Datei mit dem Namen out. XML fungiert als Datenquelle, in der die XHTML-Daten gespeichert werden. Es gibt zwei Webmethoden, die verfügbar gemacht werden, damit eine Clientanwendung mit der XHTML-Datenquelle `getXhtml` verbunden `setXhtml`werden kann: und. Die `getXhtml` Webdienstmethode gibt einen **XmlNode** zurück, der den XHTML-Code enthält, der an ein InfoPath-Rich-Text-Feld-Steuerelement gebunden werden kann. Die `setXhtml` Webdienstmethode akzeptiert eine **XmlNode** als Daten, die in der Datei out. XML gespeichert werden sollen. 
  
> [!NOTE]
> Diese Webmethoden erfordern **using** -Anweisungen, die auf die Namespaces **System.IO** und **System. XML** verweisen. 
  
Die `getXhtml` Webdienstmethode versucht, die XML-Daten, die von der out. XML-Datei zurückgegeben werden sollen, in den Datenordner auf Laufwerk C zu laden. Wenn ein Fehler auftritt, da die Datei nicht gefunden wird oder keinen gültigen XML-Code enthält, gibt die Methode ein leeres **div** -HTML-Element zurück, das auf den XHTML-Namespace verweist. 
  
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

Die `setXhtml` Webdienstmethode akzeptiert XHTML aus einem **Rich-Text-Feld** -Steuerelement in einem InfoPath-Formular. Da Webdienste keine Knotenliste unterstützen, wird beim Senden eines Rich-Text-Felds mit mehreren Zeilen an einen Webdienst der Webdienst nur die erste Zeile akzeptiert und den Rest ignoriert. 
  
Die Sample `setXhtml` -Methode geht davon aus, dass Sie einen XML-Knoten auf oberster Ebene empfängt, der in den meisten Fällen in einem **div** -Element umbrochen wird. Wenn der empfangene XML-Code kein Wrapping-Element enthält, beispielsweise wenn Text im **Rich-Textfeld** -Steuerelement keine Formatierung aufweist, kann diese Methode dies erkennen, indem Sie überprüft, ob die **NodeType** -Eigenschaft angibt, dass der übergebene XML-Code ein Textknoten ist. Wenn die XML ein Textknoten ist, erstellt die Methode ein **div** -Element und kopiert den Inhalt des Textknotens in das **div** , sodass das **div** -Objekt einen Textknoten untergeordnet mit dem Text enthält, der an den Webdienst gesendet wurde. Der von dieser Methode empfangene XML-Code wird in die Out. XML-Datei im Datenordner auf dem Laufwerk C geschrieben. 
  
> [!NOTE]
> Die Sample `setXhtml` -Methode wurde so geschrieben, dass Sie XHTML-Daten beliebiger Größe akzeptiert. In der Praxis sollten Sie immer überprüfen, wie viele Daten übertragen werden und eine Höchstgrenze für die Menge der übertragenen Daten festlegen. 
  
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
    
11. Klicken Sie auf **ändern**, erweitern Sie den Ordner dataFields, erweitern Sie den Ordner **S0: getXhtmlResponse** , erweitern Sie den Ordner **** **nacheinander** , wählen Sie das **MyRichTextElement** -Element aus, und klicken Sie dann auf **weiter**.
    
12. Klicken Sie auf **Fertig stellen**.
    
13. Erweitern Sie im Aufgabenbereich **Felder** den Ordner **dataFields**. 
    
14. Erweitern Sie die Ordner **s0:getXhtmlResponse** und **getXhtmlResult**, und ziehen Sie dann das **MyRichTextElement**-Element auf das Formular. InfoPath erkennt, dass das **MyRichTextElement** -Element ein XHTML-Element ist und ein Rich-Text-Feld-Steuerelement zum Binden daran verwendet. 
    
15. Speichern oder veröffentlichen Sie das Formular.
    
Zum Testen des Formulars öffnen Sie das Formular, geben Sie einige Rich-Text-Inhalte wie Bilder, Tabellen und formatierten Text ein. Klicken Sie auf dem Menüband auf über **Mitteln** , um den Rich-Text-Inhalt in der XML-Datei auf dem Server zu speichern. Klicken Sie auf der Registerkarte **Ansicht** auf **Abfrage** , und klicken Sie dann auf die Schaltfläche **Abfrage ausführen** auf dem Formular. Das **Rich-Textfeld** -Steuerelement sollte den XHTML-Inhalt aus der Datei out. XML anzeigen. Wenn das Rich-Text-Feld mehrere Zeilen enthält, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest. 
  

