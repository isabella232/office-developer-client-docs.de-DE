---
title: Rich-Text und Webdienste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath unterstützt binden ein Feld für Rich-Text-Steuerelement in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und Senden von Daten aus einem Feld rich-Text-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss das Format Extensible HyperText Markup Language (XHTML) entsprechen. Beispielsweise würde das Schema für ein Element namens MyRichTextElement, die rich-Text enthält die folgenden XML-Schemadefinition haben:'
ms.openlocfilehash: 07a7a3dbc0f054160adce54e316b01797feacd8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790833"
---
# <a name="rich-text-and-web-services"></a>Rich-Text und Webdienste

Microsoft InfoPath unterstützt binden ein **Feld für Rich-Text** -Steuerelement in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und Senden von Daten aus einem Feld rich-Text-Steuerelement an ein XML-Element über einen Webdienst. Das Element muss das Format Extensible HyperText Markup Language (XHTML) entsprechen. Beispielsweise das Schema für ein Element namens `MyRichTextElement` , enthält Rich Text müssten die folgenden XML-Schemadefinition: 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

Bevor Sie mit dem XHTML-Element ein **Feld für Rich-Text** -Steuerelement gebunden werden kann, sollte das Element mit einem Wrapperknoten umbrochen werden; dieser Wrapperknoten kann zu einem beliebigen Namespace gehören. Der Wrapperknoten kann wie folgt aussehen: 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

In diesem Thema wird das Erstellen eines Webdiensts an, das Senden und Empfangen von XHTML und Verwendung von InfoPath zum Binden an die Webdienstparameter kann Verfahren erläutert. Dieses Thema bietet keine ausführliche Anweisungen zum solche einen Webdienst zu erstellen. Es wird davon ausgegangen, dass Sie bereits mit arbeiten mit Webdiensten vertraut sind.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML

Das Beispiel-Webdienst wird die XHTML-Daten, die gesendet und Empfangen einer XML-Datei auf dem Server gespeichert. Diese Datei mit dem Namen out.xml, fungiert als Datenquelle, die die XHTML-Daten gespeichert werden. Es gibt zwei Webmethoden, die verfügbar gemacht werden, um eine Clientanwendung als Schnittstelle mit der XHTML-Datenquelle zu ermöglichen: `getXhtml` und `setXhtml`. Die `getXhtml` -Webdienst-Methode gibt ein **XmlNode** , der die XHTML enthält, das an ein InfoPath-rich-Text-Steuerelement gebunden werden können. Die `setXhtml` -Webdienst-Methode akzeptiert einen **XmlNode** wie die Daten in der Datei out.xml gespeichert. 
  
> [!NOTE]
> Für diese Webmethoden erfordern **using** -Anweisungen, die die Namespaces **System.IO** und **System.Xml** verwiesen. 
  
Die `getXhtml` -Webdienst-Methode versucht, laden die XML-Daten aus der Datei out.xml in den Ordner Daten zurückgegeben werden soll, auf Laufwerk c: festgelegt. Schlägt fehl, da die Datei nicht gefunden wurde oder enthält keine gültigen XML-Code, gibt die Methode ein leeres HTML **DIV** -Element zurück, das den XHTML-Namespace verweist. 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "http://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "http://someNameSpace"); 
 
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
                tempDocument.LoadXml("<div xmlns=\"http://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

Die `setXhtml` -Webdienst-Methode akzeptiert XHTML aus einem **Feld für Rich-Text** -Steuerelement in einem InfoPath-Formular. Da Webdienste nicht Knotenliste unterstützt werden, wenn ein rich-Text-Feld, mehrere Zeilen enthält, mit einem Webdienst gesendet wird, wird der Webdienst nur die erste Zeile akzeptiert und ignoriert den Rest. 
  
Im Beispiel `setXhtml` Methode wird davon ausgegangen, dass sie einen XML-Knoten auf oberster Ebene, empfangen wird, der in den meisten Fällen wird in einem **DIV** -Element eingeschlossen werden. Wenn das empfangene XML kein Umbruch-Element enthält, beispielsweise wenn Text in das **Feld für Rich-Text** -Steuerelement keine Formatierung aufweist, diese Methode erkannt, indem Sie überprüfen, ob die **NodeType** -Eigenschaft gibt an, dass das übergebene XML ein Textknoten ist. Wenn der XML-Code ein Textknoten ist, wird die Methode ein **DIV** -Element erstellt und kopiert den Inhalt der Text-Knoten in das **DIV** , sodass das **DIV** einen untergeordneten Textknoten mit dem Text enthält, an den Webdienst gesendet wurde. Das von dieser Methode empfangene XML wird in der out.xml-Datei in den Ordner Daten auf Laufwerk c: geschrieben. 
  
> [!NOTE]
> Im Beispiel `setXhtml` Methode wurde geschrieben, um XHTML-Daten beliebiger Größe zu akzeptieren. In der Praxis, Sie sollten immer überprüfen, um festzustellen, wie viele Daten übermittelt, und legen Sie eine Obergrenze für wie viele Daten, die gesendet werden können. 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
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

1. Öffnen Sie im InfoPath-Formular-Designer.
    
2. Doppelklicken Sie auf der Registerkarte **neu** auf **Webdienst** unter **Erweiterte Formularvorlagen**.
    
3. Klicken Sie im Dialogfeld **Datenverbindungs-Assistenten** wählen Sie **Daten empfangen**aus, und klicken Sie dann auf **Weiter**.
    
4. Geben Sie die Adresse des Webdiensts, die die Beispiel-Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**. 
    
5. Wählen Sie für die Empfangsmethode **GetXhtml** als Vorgang aus, und klicken Sie dann auf **Weiter**.
    
6. **GetXHTML** Webdienstmethode akzeptiert keine Parameter, klicken Sie auf **Weiter**.
    
7. Klicken Sie auf **Fertig stellen**.
    
8. Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Übermittlungsaktionen** auf **An andere Speicherorte**und klicken Sie dann auf **Webdienst** , um den gleichen Webdienst zum Senden von Daten verwenden. 
    
9. Geben Sie die Adresse des Webdiensts, die die Beispiel-Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.
    
10. Wählen Sie **SetXhtml** als Vorgang für die Submit-Methode, und klicken Sie dann auf **Weiter**.
    
11. Klicken Sie auf **Ändern**, erweitern Sie den Ordner **DataFields** , erweitern Sie den Ordner **S0: getXhtmlResponse** , erweitern Sie den Ordner **GetXhtmlResult** , wählen Sie das **MyRichTextElement** -Element, und klicken Sie dann auf **Weiter**.
    
12. Klicken Sie auf **Fertig stellen**.
    
13. Erweitern Sie im Aufgabenbereich **Felder** den Ordner **DataFields** . 
    
14. Erweitern Sie den Ordner **S0: getXhtmlResponse** und **GetXhtmlResult** , und ziehen Sie das **MyRichTextElement** -Element in das Formular. InfoPath erkennt, dass das **MyRichTextElement** -Element ein Element der XHTML ist und ein rich-Text-Steuerelement verwendet gebunden. 
    
15. Speichern oder veröffentlichen Sie das Formular.
    
Zum Testen des Formulars beim Öffnen Sie des Formulars, geben Sie einige rich-Text-Inhalt wie Bilder, Tabellen und formatierten Text. Klicken Sie auf **Absenden** auf dem Menüband die rich-Text-Inhalte in der Datei out.xml auf dem Server zu speichern. Klicken Sie auf der Registerkarte **Ansicht** auf **Abfrage** , und klicken Sie dann auf die Schaltfläche **Abfrage ausführen** , auf dem Formular. Die XHTML-Inhalte aus der Datei out.xml sollte das **Feld für Rich-Text** -Steuerelement angezeigt werden. Wenn das rich-Text-Feld mehrere Zeilen enthält, der Webdienst nur die erste Zeile akzeptiert und ignoriert die anderen. 
  

