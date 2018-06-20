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
# <a name="rich-text-and-web-services"></a><span data-ttu-id="33c09-105">Rich-Text und Webdienste</span><span class="sxs-lookup"><span data-stu-id="33c09-105">Rich Text and Web Services</span></span>

<span data-ttu-id="33c09-106">Microsoft InfoPath unterstützt binden ein **Feld für Rich-Text** -Steuerelement in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und Senden von Daten aus einem Feld rich-Text-Steuerelement an ein XML-Element über einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="33c09-106">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service.</span></span> <span data-ttu-id="33c09-107">Das Element muss das Format Extensible HyperText Markup Language (XHTML) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="33c09-107">The element must adhere to the Extensible HyperText Markup Language (XHTML) format.</span></span> <span data-ttu-id="33c09-108">Beispielsweise das Schema für ein Element namens `MyRichTextElement` , enthält Rich Text müssten die folgenden XML-Schemadefinition:</span><span class="sxs-lookup"><span data-stu-id="33c09-108">For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
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

<span data-ttu-id="33c09-109">Bevor Sie mit dem XHTML-Element ein **Feld für Rich-Text** -Steuerelement gebunden werden kann, sollte das Element mit einem Wrapperknoten umbrochen werden; dieser Wrapperknoten kann zu einem beliebigen Namespace gehören.</span><span class="sxs-lookup"><span data-stu-id="33c09-109">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace.</span></span> <span data-ttu-id="33c09-110">Der Wrapperknoten kann wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="33c09-110">The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="33c09-111">In diesem Thema wird das Erstellen eines Webdiensts an, das Senden und Empfangen von XHTML und Verwendung von InfoPath zum Binden an die Webdienstparameter kann Verfahren erläutert.</span><span class="sxs-lookup"><span data-stu-id="33c09-111">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters.</span></span> <span data-ttu-id="33c09-112">Dieses Thema bietet keine ausführliche Anweisungen zum solche einen Webdienst zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33c09-112">This topic does not provide detailed instructions on how to create such a Web service.</span></span> <span data-ttu-id="33c09-113">Es wird davon ausgegangen, dass Sie bereits mit arbeiten mit Webdiensten vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="33c09-113">It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="33c09-114">Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML</span><span class="sxs-lookup"><span data-stu-id="33c09-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="33c09-115">Das Beispiel-Webdienst wird die XHTML-Daten, die gesendet und Empfangen einer XML-Datei auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33c09-115">The example Web service stores the XHTML data that it sends and receives in an XML file on the server.</span></span> <span data-ttu-id="33c09-116">Diese Datei mit dem Namen out.xml, fungiert als Datenquelle, die die XHTML-Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="33c09-116">This file that is named out.xml, acts as a data source that stores the XHTML data.</span></span> <span data-ttu-id="33c09-117">Es gibt zwei Webmethoden, die verfügbar gemacht werden, um eine Clientanwendung als Schnittstelle mit der XHTML-Datenquelle zu ermöglichen: `getXhtml` und `setXhtml`.</span><span class="sxs-lookup"><span data-stu-id="33c09-117">There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`.</span></span> <span data-ttu-id="33c09-118">Die `getXhtml` -Webdienst-Methode gibt ein **XmlNode** , der die XHTML enthält, das an ein InfoPath-rich-Text-Steuerelement gebunden werden können.</span><span class="sxs-lookup"><span data-stu-id="33c09-118">The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control.</span></span> <span data-ttu-id="33c09-119">Die `setXhtml` -Webdienst-Methode akzeptiert einen **XmlNode** wie die Daten in der Datei out.xml gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33c09-119">The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33c09-120">Für diese Webmethoden erfordern **using** -Anweisungen, die die Namespaces **System.IO** und **System.Xml** verwiesen.</span><span class="sxs-lookup"><span data-stu-id="33c09-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="33c09-121">Die `getXhtml` -Webdienst-Methode versucht, laden die XML-Daten aus der Datei out.xml in den Ordner Daten zurückgegeben werden soll, auf Laufwerk c: festgelegt. Schlägt fehl, da die Datei nicht gefunden wurde oder enthält keine gültigen XML-Code, gibt die Methode ein leeres HTML **DIV** -Element zurück, das den XHTML-Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="33c09-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
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

<span data-ttu-id="33c09-122">Die `setXhtml` -Webdienst-Methode akzeptiert XHTML aus einem **Feld für Rich-Text** -Steuerelement in einem InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="33c09-122">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form.</span></span> <span data-ttu-id="33c09-123">Da Webdienste nicht Knotenliste unterstützt werden, wenn ein rich-Text-Feld, mehrere Zeilen enthält, mit einem Webdienst gesendet wird, wird der Webdienst nur die erste Zeile akzeptiert und ignoriert den Rest.</span><span class="sxs-lookup"><span data-stu-id="33c09-123">Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="33c09-124">Im Beispiel `setXhtml` Methode wird davon ausgegangen, dass sie einen XML-Knoten auf oberster Ebene, empfangen wird, der in den meisten Fällen wird in einem **DIV** -Element eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="33c09-124">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element.</span></span> <span data-ttu-id="33c09-125">Wenn das empfangene XML kein Umbruch-Element enthält, beispielsweise wenn Text in das **Feld für Rich-Text** -Steuerelement keine Formatierung aufweist, diese Methode erkannt, indem Sie überprüfen, ob die **NodeType** -Eigenschaft gibt an, dass das übergebene XML ein Textknoten ist.</span><span class="sxs-lookup"><span data-stu-id="33c09-125">If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node.</span></span> <span data-ttu-id="33c09-126">Wenn der XML-Code ein Textknoten ist, wird die Methode ein **DIV** -Element erstellt und kopiert den Inhalt der Text-Knoten in das **DIV** , sodass das **DIV** einen untergeordneten Textknoten mit dem Text enthält, an den Webdienst gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="33c09-126">If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service.</span></span> <span data-ttu-id="33c09-127">Das von dieser Methode empfangene XML wird in der out.xml-Datei in den Ordner Daten auf Laufwerk c: geschrieben.</span><span class="sxs-lookup"><span data-stu-id="33c09-127">The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33c09-128">Im Beispiel `setXhtml` Methode wurde geschrieben, um XHTML-Daten beliebiger Größe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="33c09-128">The sample  `setXhtml` method was written to accept XHTML data of any size.</span></span> <span data-ttu-id="33c09-129">In der Praxis, Sie sollten immer überprüfen, um festzustellen, wie viele Daten übermittelt, und legen Sie eine Obergrenze für wie viele Daten, die gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="33c09-129">In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="33c09-130">Erstellen eines InfoPath-Formulars zum Austauschen von Daten mit dem Beispielwebdienst</span><span class="sxs-lookup"><span data-stu-id="33c09-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="33c09-131">Führen Sie die folgenden Schritte aus, um ein Formular zum Testen des Beispielwebdiensts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33c09-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="33c09-132">So erstellen Sie ein Formular, über das eine Verbindung mit dem Beispielwebdienst hergestellt wird</span><span class="sxs-lookup"><span data-stu-id="33c09-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="33c09-133">Öffnen Sie im InfoPath-Formular-Designer.</span><span class="sxs-lookup"><span data-stu-id="33c09-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="33c09-134">Doppelklicken Sie auf der Registerkarte **neu** auf **Webdienst** unter **Erweiterte Formularvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="33c09-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="33c09-135">Klicken Sie im Dialogfeld **Datenverbindungs-Assistenten** wählen Sie **Daten empfangen**aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="33c09-136">Geben Sie die Adresse des Webdiensts, die die Beispiel-Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="33c09-137">Wählen Sie für die Empfangsmethode **GetXhtml** als Vorgang aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="33c09-138">**GetXHTML** Webdienstmethode akzeptiert keine Parameter, klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="33c09-139">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="33c09-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="33c09-140">Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Übermittlungsaktionen** auf **An andere Speicherorte**und klicken Sie dann auf **Webdienst** , um den gleichen Webdienst zum Senden von Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="33c09-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="33c09-141">Geben Sie die Adresse des Webdiensts, die die Beispiel-Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="33c09-142">Wählen Sie **SetXhtml** als Vorgang für die Submit-Methode, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="33c09-143">Klicken Sie auf **Ändern**, erweitern Sie den Ordner **DataFields** , erweitern Sie den Ordner **S0: getXhtmlResponse** , erweitern Sie den Ordner **GetXhtmlResult** , wählen Sie das **MyRichTextElement** -Element, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="33c09-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="33c09-144">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="33c09-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="33c09-145">Erweitern Sie im Aufgabenbereich **Felder** den Ordner **DataFields** .</span><span class="sxs-lookup"><span data-stu-id="33c09-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="33c09-146">Erweitern Sie den Ordner **S0: getXhtmlResponse** und **GetXhtmlResult** , und ziehen Sie das **MyRichTextElement** -Element in das Formular.</span><span class="sxs-lookup"><span data-stu-id="33c09-146">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form.</span></span> <span data-ttu-id="33c09-147">InfoPath erkennt, dass das **MyRichTextElement** -Element ein Element der XHTML ist und ein rich-Text-Steuerelement verwendet gebunden.</span><span class="sxs-lookup"><span data-stu-id="33c09-147">InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="33c09-148">Speichern oder veröffentlichen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="33c09-148">Save or publish the form.</span></span>
    
<span data-ttu-id="33c09-149">Zum Testen des Formulars beim Öffnen Sie des Formulars, geben Sie einige rich-Text-Inhalt wie Bilder, Tabellen und formatierten Text.</span><span class="sxs-lookup"><span data-stu-id="33c09-149">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text.</span></span> <span data-ttu-id="33c09-150">Klicken Sie auf **Absenden** auf dem Menüband die rich-Text-Inhalte in der Datei out.xml auf dem Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="33c09-150">Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server.</span></span> <span data-ttu-id="33c09-151">Klicken Sie auf der Registerkarte **Ansicht** auf **Abfrage** , und klicken Sie dann auf die Schaltfläche **Abfrage ausführen** , auf dem Formular.</span><span class="sxs-lookup"><span data-stu-id="33c09-151">Click **Query** on the **View** tab, and then click the **Run Query** button on the form.</span></span> <span data-ttu-id="33c09-152">Die XHTML-Inhalte aus der Datei out.xml sollte das **Feld für Rich-Text** -Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33c09-152">The **Rich Text Box** control should display the XHTML content from the out.xml file.</span></span> <span data-ttu-id="33c09-153">Wenn das rich-Text-Feld mehrere Zeilen enthält, der Webdienst nur die erste Zeile akzeptiert und ignoriert die anderen.</span><span class="sxs-lookup"><span data-stu-id="33c09-153">If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

