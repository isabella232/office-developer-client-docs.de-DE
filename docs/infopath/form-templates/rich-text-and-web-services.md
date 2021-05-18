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
# <a name="rich-text-and-web-services"></a><span data-ttu-id="544d0-105">Rich-Text und Webdienste</span><span class="sxs-lookup"><span data-stu-id="544d0-105">Rich Text and Web Services</span></span>

<span data-ttu-id="544d0-106">Microsoft InfoPath unterstützt das Binden eines **Rich-Text-Box-Steuerelements** in einem Formular an ein XML-Element, das von einem Webdienst empfangen wird, und das Übermitteln von Daten aus einem Rich-Text-Box-Steuerelement an ein XML-Element über einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="544d0-106">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service.</span></span> <span data-ttu-id="544d0-107">Das Element muss das Format Extensible HyperText Markup Language (XHTML) einhalten.</span><span class="sxs-lookup"><span data-stu-id="544d0-107">The element must adhere to the Extensible HyperText Markup Language (XHTML) format.</span></span> <span data-ttu-id="544d0-108">Das Schema für ein Element mit dem Namen Rich Text hat beispielsweise die  `MyRichTextElement` folgende XML-Schemadefinition:</span><span class="sxs-lookup"><span data-stu-id="544d0-108">For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
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

<span data-ttu-id="544d0-p103">Bevor ein **Feld für Rich-Text**-Steuerelement an das XHTML-Element gebunden werden kann, muss das Element mit einem Wrapperknoten gepackt werden; dieser Wrapperknoten kann zu einem beliebigen Namespace gehören. Der Wrapperknoten kann so aussehen:</span><span class="sxs-lookup"><span data-stu-id="544d0-p103">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace. The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="544d0-111">In diesem Thema wird das Erstellen eines Webdiensts beschrieben, der XHTML senden und empfangen kann, sowie die Verwendung von InfoPath zum Binden an die Webdienstparameter.</span><span class="sxs-lookup"><span data-stu-id="544d0-111">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters.</span></span> <span data-ttu-id="544d0-112">Dieses Thema enthält keine detaillierten Anweisungen zum Erstellen eines solchen Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="544d0-112">This topic does not provide detailed instructions on how to create such a Web service.</span></span> <span data-ttu-id="544d0-113">Es wird davon ausgegangen, dass Sie bereits mit der Arbeit mit Webdiensten vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="544d0-113">It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="544d0-114">Entwerfen eines Webdiensts zum Empfangen und Senden von XHTML</span><span class="sxs-lookup"><span data-stu-id="544d0-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="544d0-115">Der Beispielwebdienst speichert die XHTML-Daten, die er sendet und empfängt, in einer XML-Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="544d0-115">The example Web service stores the XHTML data that it sends and receives in an XML file on the server.</span></span> <span data-ttu-id="544d0-116">Diese Datei mit dem Namen out.xml als Datenquelle, in der die XHTML-Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="544d0-116">This file that is named out.xml, acts as a data source that stores the XHTML data.</span></span> <span data-ttu-id="544d0-117">Es gibt zwei Webmethoden, die verfügbar gemacht werden, damit eine Clientanwendung eine Schnittstelle mit der XHTML-Datenquelle verwenden kann:  `getXhtml` und  `setXhtml` .</span><span class="sxs-lookup"><span data-stu-id="544d0-117">There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`.</span></span> <span data-ttu-id="544d0-118">Die Webdienstmethode gibt eine XmlNode zurück, die XHTML enthält, die an ein `getXhtml` InfoPath-Rich-Text-Feldsteuerelement gebunden werden kann. </span><span class="sxs-lookup"><span data-stu-id="544d0-118">The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control.</span></span> <span data-ttu-id="544d0-119">Die  `setXhtml` Webdienstmethode akzeptiert ein **XmlNode-Element** als Daten, die in der Datei out.xml werden.</span><span class="sxs-lookup"><span data-stu-id="544d0-119">The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="544d0-120">Diese Webmethoden erfordern **die Verwendung von** **Anweisungen,** die auf die System.IO und **System.Xml** verweisen.</span><span class="sxs-lookup"><span data-stu-id="544d0-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="544d0-121">Die Webdienstmethode versucht, die out.xml zu laden, die aus der #out.xml im Ordner Daten auf Laufwerk `getXhtml` C zurückgegeben werden sollen. Wenn ein Fehler auftritt, da die Datei nicht gefunden wird oder keinen  gültigen XML-Code enthält, gibt die Methode ein leeres DIV-HTML-Element zurück, das auf den XHTML-Namespace verweist.</span><span class="sxs-lookup"><span data-stu-id="544d0-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
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

<span data-ttu-id="544d0-122">Die  `setXhtml` Webdienstmethode akzeptiert XHTML von einem **Rich-Text-Box-Steuerelement** in einem InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="544d0-122">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form.</span></span> <span data-ttu-id="544d0-123">Da Webdienste keine Knotenliste unterstützen, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest, wenn ein Rich-Text-Feld mit mehreren Zeilen an einen Webdienst gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="544d0-123">Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="544d0-124">Die Beispielmethode geht davon aus, dass sie einen XML-Knoten der obersten Ebene erhält, der in den meisten Fällen in ein  `setXhtml` **DIV-Element umschlossen** wird.</span><span class="sxs-lookup"><span data-stu-id="544d0-124">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element.</span></span> <span data-ttu-id="544d0-125">Wenn die empfangene XML kein Umbruchelement enthält, z. B. wenn Text im **Rich Text Box-Steuerelement** keine Formatierung enthält, erkennt diese Methode dies, indem sie überprüft, ob die **NodeType-Eigenschaft** angibt, dass die übergebene XML ein Textknoten ist.</span><span class="sxs-lookup"><span data-stu-id="544d0-125">If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node.</span></span> <span data-ttu-id="544d0-126">Wenn es sich bei der XML um einen Textknoten handelt, erstellt die Methode ein **DIV-Element** und kopiert den Textknoteninhalt in das **DIV,** sodass das **DIV** einen untergeordneten Textknoten mit dem Text enthält, der an den Webdienst gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="544d0-126">If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service.</span></span> <span data-ttu-id="544d0-127">Die von dieser Methode empfangene XML wird in die datei out.xml im Ordner Daten auf laufwerk C geschrieben.</span><span class="sxs-lookup"><span data-stu-id="544d0-127">The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="544d0-128">Die  `setXhtml` Beispielmethode wurde so geschrieben, dass sie XHTML-Daten beliebiger Größe akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="544d0-128">The sample  `setXhtml` method was written to accept XHTML data of any size.</span></span> <span data-ttu-id="544d0-129">In der Praxis sollten Sie immer überprüfen, wie viele Daten übertragen werden und eine Höchstgrenze für die Menge der übertragenen Daten festlegen.</span><span class="sxs-lookup"><span data-stu-id="544d0-129">In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="544d0-130">Erstellen eines InfoPath-Formulars zum Austauschen von Daten mit dem Beispielwebdienst</span><span class="sxs-lookup"><span data-stu-id="544d0-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="544d0-131">Führen Sie die folgenden Schritte aus, um ein Formular zum Testen des Beispielwebdiensts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="544d0-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="544d0-132">So erstellen Sie ein Formular, über das eine Verbindung mit dem Beispielwebdienst hergestellt wird</span><span class="sxs-lookup"><span data-stu-id="544d0-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="544d0-133">Öffnen Sie den InfoPath-Formular-Designer.</span><span class="sxs-lookup"><span data-stu-id="544d0-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="544d0-134">Doppelklicken Sie auf der Registerkarte **Neu** unter **Erweiterte Formularvorlagen** auf **Webdienst**.</span><span class="sxs-lookup"><span data-stu-id="544d0-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="544d0-135">Wählen Sie im Dialogfeld **Datenverbindungs-Assistent** die Option **Daten empfangen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="544d0-136">Geben Sie die Adresse des Webdiensts ein, der die Beispiele für Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**. </span><span class="sxs-lookup"><span data-stu-id="544d0-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="544d0-137">Wählen Sie **getXhtml** als Vorgang für die Empfangsmethode aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="544d0-138">Für die **getXHTML**-Webdienstmethode können keine Parameter verwendet werden. Klicken Sie daher auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="544d0-139">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="544d0-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="544d0-140">Klicken Sie auf der Registerkarte **Daten** in der Gruppe **Übermittlungsaktionen** auf **An andere Speicherorte** und dann auf **Webdienst**, um zum Senden der Daten den gleichen Webdienst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="544d0-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="544d0-141">Geben Sie die Adresse des Webdiensts ein, der die Beispiele für Webdienstmethoden enthält, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="544d0-142">Wählen Sie **setXhtml** als Vorgang für die Sendemethode aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="544d0-143">Klicken **Sie auf** Ändern, erweitern Sie den Ordner **dataFields,** erweitern Sie den **Ordner s0:getXhtmlResponse,** erweitern Sie den **Ordner getXhtmlResult,** wählen Sie das **MyRichTextElement-Element** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="544d0-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="544d0-144">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="544d0-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="544d0-145">Erweitern Sie im Aufgabenbereich **Felder** den Ordner **dataFields**.</span><span class="sxs-lookup"><span data-stu-id="544d0-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="544d0-146">Erweitern Sie die Ordner **s0:getXhtmlResponse** und **getXhtmlResult**, und ziehen Sie dann das **MyRichTextElement**-Element auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="544d0-146">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form.</span></span> <span data-ttu-id="544d0-147">InfoPath erkennt, dass das **MyRichTextElement-Element** ein XHTML-Element ist, und verwendet ein Rich-Text-Feld-Steuerelement, um eine Bindung an das Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="544d0-147">InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="544d0-148">Speichern oder veröffentlichen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="544d0-148">Save or publish the form.</span></span>
    
<span data-ttu-id="544d0-149">Um das Formular zu testen, öffnen Sie das Formular, und geben Sie einige Rich-Text-Inhalte wie Bilder, Tabellen und formatierten Text ein.</span><span class="sxs-lookup"><span data-stu-id="544d0-149">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text.</span></span> <span data-ttu-id="544d0-150">Klicken **Sie auf** dem Menüband auf Absenden, um den Rich-Text-Inhalt in der out.xml auf dem Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="544d0-150">Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server.</span></span> <span data-ttu-id="544d0-151">Klicken **Sie auf** der Registerkarte **Ansicht** auf Abfrage, und klicken Sie dann auf die **Schaltfläche** Abfrage ausführen im Formular.</span><span class="sxs-lookup"><span data-stu-id="544d0-151">Click **Query** on the **View** tab, and then click the **Run Query** button on the form.</span></span> <span data-ttu-id="544d0-152">Das **Rich Text Box-Steuerelement** sollte den XHTML-Inhalt aus der out.xml anzeigen.</span><span class="sxs-lookup"><span data-stu-id="544d0-152">The **Rich Text Box** control should display the XHTML content from the out.xml file.</span></span> <span data-ttu-id="544d0-153">Wenn das Rich-Text-Feld mehrere Zeilen enthält, akzeptiert der Webdienst nur die erste Zeile und ignoriert den Rest.</span><span class="sxs-lookup"><span data-stu-id="544d0-153">If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

