---
title: Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Das Feature Formulare zusammenführen des Microsoft InfoPath-Editors ist so konzipiert, dass die Daten aus mehreren Formularen in einem einzigen Formular kombiniert werden.
ms.openlocfilehash: f79553f7fdf0b59c77a98fd479e0a307e4f2e6a3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537801"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="efb77-103">Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen</span><span class="sxs-lookup"><span data-stu-id="efb77-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="efb77-104">Das **Feature Formulare zusammenführen** des Microsoft InfoPath-Editors ist so konzipiert, dass die Daten aus mehreren Formularen in einem einzigen Formular kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="efb77-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="efb77-105">Dieser Vorgang wird auch als Datenaggregation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="efb77-105">This is also known as data aggregation.</span></span> <span data-ttu-id="efb77-106">Wenn das Zusammenführen von Formularen  aktiviert ist, können  Sie auf die Registerkarte Datei klicken, auf Senden **speichern, &amp;** unter **Link &amp;** importieren auf Formulare zusammenführen klicken und dann auf die Schaltfläche Formulare zusammenführen klicken, um ein oder mehrere Formulare auszuwählen, die mit dem aktuell geöffneten Formular zusammengeführt werden sollen. </span><span class="sxs-lookup"><span data-stu-id="efb77-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="efb77-107">Das derzeit geöffnete Formular ist das Zielformular,  und die im Dialogfeld Formulare zusammenführen ausgewählten Formulare werden als Quellformulare bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="efb77-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="efb77-p102">Die Aggregation der Daten, die sich aus dem Zusammenführen von Formularen ergibt, kann alle Daten in den Quell- und Zielformularen oder nur einen Teil der Originaldaten einschließen. Nachstehend werden die Standardvorgänge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efb77-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="efb77-p103">Bei wiederholten Elementen werden die Daten an einer entsprechenden Position im Zieldokument eingefügt. Dies geschieht, wenn das **MaxOccurs**-Attribut des Zielelements größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="efb77-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="efb77-112">Bei nicht wiederholten Elementen (das heißt bei Elementen, bei denen **MaxOccurs** gleich "1" ist), werden die Attribute der Quellelemente den vorhandenen Attributen des Zielelements hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="efb77-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="efb77-113">Erstellen einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="efb77-113">Creating a Custom Transform</span></span>

<span data-ttu-id="efb77-114">Der Standardvorgang beim Zusammenführen von Formularen eignet sich gut für Formulare, die auf dem gleichen XML-Schema basieren.</span><span class="sxs-lookup"><span data-stu-id="efb77-114">The default operation when merging forms works well for forms that are based on the same XML schema.</span></span> <span data-ttu-id="efb77-115">In manchen Fällen möchten Sie jedoch möglicherweise Formulare zusammenführen, die auf anderen Schemas basieren oder den Standardzusammenführungsvorgang für auf dem gleichen Schema basierende Formulare außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="efb77-115">In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema.</span></span> <span data-ttu-id="efb77-116">Für diese Szenarien können Sie eine XSL-Transformation (XSLT) erstellen, die Aggregationsanweisungen für den Zusammenführungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="efb77-116">For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation.</span></span> <span data-ttu-id="efb77-117">Die Transformation wird bei der Zusammenführung angewendet, um ein DOM-Dokument zu erstellen, das die zu importierenden Informationen enthält sowie Anmerkungen, in denen angegeben wird, wie diese Informationen in das Zieldokument integriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="efb77-117">The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document.</span></span> <span data-ttu-id="efb77-118">Diese Anmerkungen sind XML-Attribute im Namespace  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` .</span><span class="sxs-lookup"><span data-stu-id="efb77-118">These annotations are XML attributes in the namespace  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="efb77-p105">Die XML-Attribute und die entsprechenden Werte dienen als Aggregationsanweisungen für die Zusammenführung der einzelnen Knoten mit dem XML-Zieldokument. Diese Attribute werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efb77-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="efb77-121">select</span><span class="sxs-lookup"><span data-stu-id="efb77-121">select</span></span>

<span data-ttu-id="efb77-122">Das **agg:select**-Attribut enthält einen absoluten XPath-Ausdruck, durch den das Zielelement identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="efb77-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="efb77-123">insert</span><span class="sxs-lookup"><span data-stu-id="efb77-123">insert</span></span>

<span data-ttu-id="efb77-124">Der Wert "insert" für das **agg:action-Attribut** anweisen InfoPath, das Quellelement als untergeordnetes Element des Zielelements einfügen, das mithilfe des **agg:select-Attributs angegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="efb77-124">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute.</span></span> <span data-ttu-id="efb77-125">Die unterlegenen Elemente des Quellelements sind in den Einfügevorgang eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="efb77-125">The children of the source element are included in the insert operation.</span></span> <span data-ttu-id="efb77-126">Mit **dem selectChild-Attribut** können Sie einen bestimmten Speicherort für den Einfügenknotenvorgang auswählen.</span><span class="sxs-lookup"><span data-stu-id="efb77-126">The **selectChild** attribute lets you select a certain location for the insert node operation.</span></span> <span data-ttu-id="efb77-127">Das **order-Attribut** wird verwendet, um anzugeben, ob die Quellelemente vor vorhandenen Zielelementen oder danach eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="efb77-127">The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after.</span></span> <span data-ttu-id="efb77-128">Der Standardwert, wenn das **order-Attribut** nicht vorhanden ist, ist "after".</span><span class="sxs-lookup"><span data-stu-id="efb77-128">The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="efb77-129">replace</span><span class="sxs-lookup"><span data-stu-id="efb77-129">replace</span></span>

<span data-ttu-id="efb77-130">Der Wert "replace" für das **Attribut agg:action** anweisen InfoPath, jedes Zielelement, auf das durch das **select-Attribut** verwiesen wird, durch das Source-Element zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="efb77-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="efb77-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="efb77-131">mergeAttributes</span></span>

<span data-ttu-id="efb77-132">Wenn der Wert des **agg:action-Attributs** "mergeAttributes" ist, werden die Attribute des Quellelements mit den Attributen der einzelnen Zielelemente zusammengeführt, auf die das **select-Attribut** verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="efb77-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="efb77-133">Löschen</span><span class="sxs-lookup"><span data-stu-id="efb77-133">delete</span></span>

<span data-ttu-id="efb77-134">Wenn der Wert des **agg:action-Attributs** "delete" ist, werden alle Zielelemente, auf die durch das **select-Attribut** verwiesen wird, aus dem Zieldokument gelöscht.</span><span class="sxs-lookup"><span data-stu-id="efb77-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="efb77-135">In Verbindung mit den im Namespace angegebenen Attributen verwenden Sie den Namespace, um ein XSL-Objekt zu bezeichnen, das die `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` Schnittstelle **IXMLDOMDocument implementiert.**</span><span class="sxs-lookup"><span data-stu-id="efb77-135">In conjunction with the attributes specified in the  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**.</span></span> <span data-ttu-id="efb77-136">Eines der nützlichsten Member dieser Schnittstelle ist die **get-documentElement**-Methode.</span><span class="sxs-lookup"><span data-stu-id="efb77-136">One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="efb77-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="efb77-137">get-documentElement</span></span>

<span data-ttu-id="efb77-p108">Die **target:get-documentElement**-Funktion ermöglicht den Zugriff auf das DOM (Document Object Model) des Zieldokuments. Damit kann die Funktionsweise des Zusammenführungsvorgangs basierend auf dem aktuellen Inhalt des Zieldokuments geändert werden.   
 
</span><span class="sxs-lookup"><span data-stu-id="efb77-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="efb77-140">Schritte zum Erstellen einer benutzerdefinierten Zusammenführung</span><span class="sxs-lookup"><span data-stu-id="efb77-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="efb77-p109">Wählen Sie die Typen der XML-Quelldokumente aus, aus denen Sie Daten zusammenführen möchten. Sammeln Sie repräsentative Beispiele für die einzelnen Quelldokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="efb77-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="efb77-143">Leiten Sie das XML-Schema für jede Art von XML-Quelldokument für ein vorhandenes InfoPath-Formular ab.</span><span class="sxs-lookup"><span data-stu-id="efb77-143">Derive the XML schema for each kind of XML source document for an existing InfoPath form.</span></span> <span data-ttu-id="efb77-144">Dieser Schritt kann problemlos durch Exportieren des XML-Schemas mit dem Befehl **Quelldateien** exportieren auf der Registerkarte **Veröffentlichen** der Backstage ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="efb77-144">This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage.</span></span> <span data-ttu-id="efb77-145">Für XML-Dokumente, die nicht in InfoPath erstellt wurden, können Sie ein Tool wie Microsoft Visual Studio verwenden, um ein Schema aus dem XML-Beispieldokument zu erstellen, oder Sie können ein Beispielformular aus dem XML-Dokument in InfoPath erstellen und dann das Schema exportieren, das InfoPath aus der Dokumentstruktur ab leitet.</span><span class="sxs-lookup"><span data-stu-id="efb77-145">For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="efb77-146">Identifizieren Sie die Daten, die Sie aus den einzelnen XML-Quelldokumenttypen zusammenführen möchten.</span><span class="sxs-lookup"><span data-stu-id="efb77-146">Identify the data that you want to merge from each kind of XML source document.</span></span> <span data-ttu-id="efb77-147">Dieser Schritt hängt fast vollständig von den Anforderungen der Quell- und Zielformulare ab.</span><span class="sxs-lookup"><span data-stu-id="efb77-147">This step will depend almost entirely on the requirements of both your source and destination forms.</span></span> <span data-ttu-id="efb77-148">Bei manchen Formularen möchten Sie möglicherweise alle Daten aus dem Quellformular kopieren.</span><span class="sxs-lookup"><span data-stu-id="efb77-148">For some forms, you may want to copy all of the data from the source form.</span></span> <span data-ttu-id="efb77-149">Bei anderen benötigen Sie möglicherweise nur ein oder zwei Elemente aus dem dem Formular zugrunde liegenden XML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="efb77-149">For others, you may want only one or two elements from the form's underlying XML document.</span></span> <span data-ttu-id="efb77-150">Achten Sie beim Identifizieren der zusammenzuführenden Daten besonders auf die Quell- und Zieldokumente, um sicherzustellen, dass die Elemente zwischen den beiden Formularen logisch zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="efb77-150">When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="efb77-151">Erstellen Sie für jeden XML-Quelldokumenttyp eine XSL-Transformation.</span><span class="sxs-lookup"><span data-stu-id="efb77-151">Create an XSL transform for each kind of XML source document.</span></span> <span data-ttu-id="efb77-152">Dieser Schritt beansprucht beim Konfigurieren der Zusammenführung von Formularen die meiste Zeit.</span><span class="sxs-lookup"><span data-stu-id="efb77-152">When configuring the merging of your forms, this step will take the most time.</span></span> <span data-ttu-id="efb77-153">Der Zweck der XSL-Transformation besteht darin, das XML-Quelldokument in ein Format zu transformieren, das mit dem Zielformular zusammengeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="efb77-153">The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form.</span></span> <span data-ttu-id="efb77-154">Entscheiden Sie beim Entwerfen der Transformation, ob Sie das Zusammenführen von XML-Speicherortpfaden oder das Zusammenführen aus InfoPath-Aggregationsanweisungen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="efb77-154">When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="efb77-155">Visual Studio ist ein praktisches Tool zum Erstellen von XSL-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="efb77-155">Visual Studio is a convenient tool for creating XSL transforms.</span></span> <span data-ttu-id="efb77-156">Visual Studio enthält syntax coloring und eine Dokumentgliederung.</span><span class="sxs-lookup"><span data-stu-id="efb77-156">Visual Studio provides syntax coloring and a document outline.</span></span> <span data-ttu-id="efb77-157">Außerdem werden automatisch schließende Tags für die XSL-Elemente bereitgestellt, sodass Sie redundante Eingaben und schwer zu findende Rechtschreibfehler vermeiden können.</span><span class="sxs-lookup"><span data-stu-id="efb77-157">It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors.</span></span> <span data-ttu-id="efb77-158">Sie können XSL-Transformationen auch mit einem Text-Editor wie beispielsweise Editor erstellen.</span><span class="sxs-lookup"><span data-stu-id="efb77-158">You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="efb77-159">Beginnen Sie mit der Identitätstransformation, bei der es sich einfach um eine XSL-Transformation handelt, mit der die eingegebene XML-Datei ausgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="efb77-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    <span data-ttu-id="efb77-160">Fügen Sie dann überschriebene Vorlagenabschnitte für die Elemente hinzu, für die Sie eine spezielle Behandlung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="efb77-160">Then add overriding template sections for the elements you want to add special handling for.</span></span> <span data-ttu-id="efb77-161">Beispielsweise ändert diese Vorlage ein Element in ein Element und legt den Wert des  `<src:Task>`  `<my:field1>` **Attributs agg:action** auf "replace" fest.</span><span class="sxs-lookup"><span data-stu-id="efb77-161">For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="efb77-162">Fügen Sie die XSL-Transformationsdateien und Schemadateien in der Formularvorlage hinzu.</span><span class="sxs-lookup"><span data-stu-id="efb77-162">Add the XSL transform files and schema files in the form template.</span></span> <span data-ttu-id="efb77-163">Nachdem Sie Schemas für jede Art von Quelldokument abgeleitet und eine XSL-Transformation erstellt haben, um jeden Dokumenttyp zu konvertieren, damit InfoPath seine Daten zusammenführen kann, fügen Sie sie dem Formular als Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="efb77-163">After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form.</span></span> <span data-ttu-id="efb77-164">Klicken **Sie auf** der Registerkarte **Daten**  auf Ressourcendateien, und klicken Sie dann im Dialogfeld Ressourcendateien auf Hinzufügen, navigieren Sie zu Ihrem Schema oder ihrer XSL-Transformationsdatei, und klicken Sie dann auf **OK**. </span><span class="sxs-lookup"><span data-stu-id="efb77-164">Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**.</span></span> <span data-ttu-id="efb77-165">Gehen Sie wie für jede erstellte Schemadatei und XSL-Transformationsdatei vor.</span><span class="sxs-lookup"><span data-stu-id="efb77-165">Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="efb77-166">Wenn die hinzugefügten Schemas das **targetNamespace-Attribut** verwenden, müssen Sie der XSF-Datei des Formulars ein Eigenschaftselement hinzufügen, damit InfoPath den Namespace des Schemas kennt.</span><span class="sxs-lookup"><span data-stu-id="efb77-166">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema.</span></span> <span data-ttu-id="efb77-167">Zum Zugreifen auf diese Datei klicken Sie auf die Registerkarte **Datei**, auf **Veröffentlichen** und dann auf **Quelldateien exportieren**.</span><span class="sxs-lookup"><span data-stu-id="efb77-167">To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**.</span></span> <span data-ttu-id="efb77-168">Wählen Sie einen Speicherort für die Dateien aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="efb77-168">Select a location for the files, and then click **OK**.</span></span> <span data-ttu-id="efb77-169">Schließen Sie dann die InfoPath-Formularvorlage, die Sie entwerfen.</span><span class="sxs-lookup"><span data-stu-id="efb77-169">Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="efb77-170">Navigieren Sie zu dem Speicherort, den Sie für die extrahierten Dateien angegeben haben, und suchen Sie nach der Datei mit der Dateinamenerweiterung XSF.</span><span class="sxs-lookup"><span data-stu-id="efb77-170">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension.</span></span> <span data-ttu-id="efb77-171">In der Regel wird diese Datei manifest.xsf genannt.</span><span class="sxs-lookup"><span data-stu-id="efb77-171">Usually, this file is called manifest.xsf.</span></span> <span data-ttu-id="efb77-172">Öffnen Sie die Datei in Editor, suchen Sie nach dem Tag, das Ihrem Schema entspricht, und fügen Sie ein "Namespace"-Eigenschaftselement hinzu, um den `<xsf:file>` **targetNamespace** anzugeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="efb77-172">Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="efb77-173">Der letzte Schritt beim Vorbereiten des Formulars für die Unterstützung der benutzerdefinierten Zusammenführung besteht darin, das **importParameters**-Element in der dem Formular zugeordneten XSF-Datei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="efb77-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="efb77-174">Suchen Sie zunächst das  `<xsf:importParameters>` Tag in der XSF-Datei.</span><span class="sxs-lookup"><span data-stu-id="efb77-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="efb77-175">Fügen Sie für jedes Schema-/XSL-Transformationspaar, das Sie für Ihr Formular erstellt haben, dem **xsf:importParameters-Element** ein **xsf:importSource-Element** hinzu: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>` .</span><span class="sxs-lookup"><span data-stu-id="efb77-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="efb77-176">Das **Name-Attribut** des **xsf:importSource-Elements** enthält den Namen der Formularvorlage, der in einem Quell-XML-Dokument enthalten sein kann.</span><span class="sxs-lookup"><span data-stu-id="efb77-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="efb77-177">Normalerweise lassen Sie dies leer.</span><span class="sxs-lookup"><span data-stu-id="efb77-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="efb77-178">Das **schema**-Attribut enthält den Namen einer Schemadatei, die Sie der Formularvorlage im vorherigen Schritt hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="efb77-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="efb77-179">Das **transform**-Attribut schließlich enthält den Namen der XSL-Transformation, die Sie zum Konvertieren von dem Schema entsprechenden Formularen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="efb77-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="efb77-180">Sie können eine benutzerdefinierte Transformation entweder mit dem [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) oder allein verwenden.</span><span class="sxs-lookup"><span data-stu-id="efb77-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="efb77-181">Erstellen einer benutzerdefinierten Zusammenführung in Code</span><span class="sxs-lookup"><span data-stu-id="efb77-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="efb77-182">Das benutzerdefinierte Zusammenführen mit [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) Code wird mithilfe des Merge-Ereignishandlers mit dem entsprechenden **useScriptHandler-Attribut** des **importParameters-Elements** in der dem Formular zugeordneten XSF-Datei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="efb77-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="efb77-183">Im verwalteten Code können Sie das Merge-Ereignis aktivieren, indem Sie das  Kontrollkästchen Zusammenführen  mit benutzerdefiniertem Code aktivieren und dann in der Kategorie Erweitert des Dialogfelds Formularoptionen, das in der Backstage verfügbar ist, auf die Schaltfläche Bearbeiten klicken. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx)  </span><span class="sxs-lookup"><span data-stu-id="efb77-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

