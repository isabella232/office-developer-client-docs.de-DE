---
title: Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Das Feature Formulare zusammenführen von Microsoft InfoPath-Editor ist darauf ausgelegt, um die Daten aus mehreren Formularen in ein einziges Formular zu kombinieren.
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386915"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="e862b-103">Aktivieren der benutzerdefinierten Zusammenführung von InfoPath-Formularen</span><span class="sxs-lookup"><span data-stu-id="e862b-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="e862b-104">Das Feature **Formulare zusammenführen** von Microsoft InfoPath-Editor ist darauf ausgelegt, um die Daten aus mehreren Formularen in ein einziges Formular zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="e862b-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="e862b-105">Dies ist auch bekannt als Datenaggregation.</span><span class="sxs-lookup"><span data-stu-id="e862b-105">This is also known as data aggregation.</span></span> <span data-ttu-id="e862b-106">Zusammenführen von Formularen aktiviert ist, können Sie klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Speichern &amp; senden**, klicken Sie auf **Das Zusammenführen von Formularen** unter **Import &amp; Link**, und klicken Sie dann auf die Schaltfläche **Formulare zusammenführen** eines oder mehrere Formulare zum Zusammenführen auswählen die zurzeit geöffnete Formular.</span><span class="sxs-lookup"><span data-stu-id="e862b-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="e862b-107">Das Formular, das zurzeit geöffnet ist ist das Ziel und die Formulare im Dialogfeld **Formulare zusammenführen** ausgewählt werden als die Quellformulare bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e862b-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="e862b-p102">Die Aggregation der Daten, die sich aus dem Zusammenführen von Formularen ergibt, kann alle Daten in den Quell- und Zielformularen oder nur einen Teil der Originaldaten einschließen. Nachstehend werden die Standardvorgänge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e862b-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="e862b-p103">Bei wiederholten Elementen werden die Daten an einer entsprechenden Position im Zieldokument eingefügt. Dies geschieht, wenn das **MaxOccurs**-Attribut des Zielelements größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="e862b-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="e862b-112">Bei nicht wiederholten Elementen (das heißt bei Elementen, bei denen **MaxOccurs** gleich "1" ist), werden die Attribute der Quellelemente den vorhandenen Attributen des Zielelements hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e862b-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="e862b-113">Erstellen einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="e862b-113">Creating a Custom Transform</span></span>

<span data-ttu-id="e862b-114">Der Standardvorgang beim Zusammenführen von Formularen eignet sich gut für Formulare, die auf das gleiche XML-Schema basieren.</span><span class="sxs-lookup"><span data-stu-id="e862b-114">The default operation when merging forms works well for forms that are based on the same XML schema.</span></span> <span data-ttu-id="e862b-115">In einigen Fällen jedoch sollten Sie Formulare, die auf verschiedenen Schemas basieren zusammengeführt oder durch Überschreiben der standardmäßigen Zusammenführungsvorgang für Formulare, die auf das gleiche Schema basieren.</span><span class="sxs-lookup"><span data-stu-id="e862b-115">In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema.</span></span> <span data-ttu-id="e862b-116">Für diese Szenarien können Sie eine XSL-Transformation (XSLT), erstellen, die Aggregation von Anweisungen für den Zusammenführungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="e862b-116">For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation.</span></span> <span data-ttu-id="e862b-117">Die Transformation Merge Zeitpunkt zum Erstellen eines DOM-Dokuments mit den Informationen, die zusammen mit Anmerkungen angeben, wie diese Informationen in das Zieldokument integrieren importiert werden.</span><span class="sxs-lookup"><span data-stu-id="e862b-117">The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document.</span></span> <span data-ttu-id="e862b-118">Diese Anmerkungen sind XML-Attribute im Namespace `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="e862b-118">These annotations are XML attributes in the namespace  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="e862b-p105">Die XML-Attribute und die entsprechenden Werte dienen als Aggregationsanweisungen für die Zusammenführung der einzelnen Knoten mit dem XML-Zieldokument. Diese Attribute werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e862b-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="e862b-121">select</span><span class="sxs-lookup"><span data-stu-id="e862b-121">select</span></span>

<span data-ttu-id="e862b-122">Das **agg:select**-Attribut enthält einen absoluten XPath-Ausdruck, durch den das Zielelement identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e862b-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="e862b-123">insert</span><span class="sxs-lookup"><span data-stu-id="e862b-123">insert</span></span>

<span data-ttu-id="e862b-124">Der Wert "Einfügen" für das **agg: Action** -Attribut weist InfoPath Quellelements als untergeordnetes Element des Zielelements einfügen, die mit dem **agg: Select** -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e862b-124">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute.</span></span> <span data-ttu-id="e862b-125">Die untergeordneten Elemente des Quellelements sind in der Einfügevorgang enthalten.</span><span class="sxs-lookup"><span data-stu-id="e862b-125">The children of the source element are included in the insert operation.</span></span> <span data-ttu-id="e862b-126">Das Attribut **SelectChild** können Sie eine bestimmte Position für den Knoteneinfügevorgang auswählen.</span><span class="sxs-lookup"><span data-stu-id="e862b-126">The **selectChild** attribute lets you select a certain location for the insert node operation.</span></span> <span data-ttu-id="e862b-127">Das **Reihenfolge** -Attribut wird verwendet, um anzugeben, ob die Quellelemente vor einer vorhandenen eingefügt werden Ziel Elemente oder nachdem.</span><span class="sxs-lookup"><span data-stu-id="e862b-127">The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after.</span></span> <span data-ttu-id="e862b-128">Der Standardwert ist das **Reihenfolge** -Attribut nicht vorhanden ist, ist "nach".</span><span class="sxs-lookup"><span data-stu-id="e862b-128">The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="e862b-129">replace</span><span class="sxs-lookup"><span data-stu-id="e862b-129">replace</span></span>

<span data-ttu-id="e862b-130">Der Wert "ersetzen" für das **agg: Action** -Attribut weist InfoPath aller Zielelemente durch das Attribut **Wählen** mit Quellelements ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e862b-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="e862b-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="e862b-131">mergeAttributes</span></span>

<span data-ttu-id="e862b-132">Wenn der Wert des agg:action-Attributs mergeAttributes entspricht, werden die Attribute des Quellelements mit den Attributen aller Zielelemente, auf die mit dem select-Attribut verwiesen wird, zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="e862b-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="e862b-133">Löschen</span><span class="sxs-lookup"><span data-stu-id="e862b-133">delete</span></span>

<span data-ttu-id="e862b-134">Wenn der Wert des agg:action-Attributs delete entspricht, werden alle Zielelemente, auf die mit dem select-Attribut verwiesen wird, aus dem Zieldokument gelöscht. </span><span class="sxs-lookup"><span data-stu-id="e862b-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="e862b-135">In Verbindung mit den Attributen angegeben, der `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` -Namespace, verwenden Sie die `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` Namespace zu versehen sind, wird ein XSL-Objekt, das die **IXMLDOMDocument**-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="e862b-135">In conjunction with the attributes specified in the  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**.</span></span> <span data-ttu-id="e862b-136">Eine der nützlichsten Elemente dieser Schnittstelle ist die Methode **Get-DocumentElement**.</span><span class="sxs-lookup"><span data-stu-id="e862b-136">One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="e862b-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="e862b-137">get-documentElement</span></span>

<span data-ttu-id="e862b-p108">Die **target:get-documentElement**-Funktion ermöglicht den Zugriff auf das DOM (Document Object Model) des Zieldokuments. Damit kann die Funktionsweise des Zusammenführungsvorgangs basierend auf dem aktuellen Inhalt des Zieldokuments geändert werden.   
 
</span><span class="sxs-lookup"><span data-stu-id="e862b-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="e862b-140">Schritte zum Erstellen einer benutzerdefinierten Zusammenführung</span><span class="sxs-lookup"><span data-stu-id="e862b-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="e862b-p109">Wählen Sie die Typen der XML-Quelldokumente aus, aus denen Sie Daten zusammenführen möchten. Sammeln Sie repräsentative Beispiele für die einzelnen Quelldokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="e862b-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="e862b-143">Leiten Sie das XML-Schema für jede Art von XML-Quelldokument für ein vorhandenes InfoPath-Formular.</span><span class="sxs-lookup"><span data-stu-id="e862b-143">Derive the XML schema for each kind of XML source document for an existing InfoPath form.</span></span> <span data-ttu-id="e862b-144">Dieser Schritt erfolgt auf einfache Weise durch Exportieren von XML-Schema mit dem Befehl **Quelldateien exportieren** auf der Registerkarte **Veröffentlichen** die Backstage-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="e862b-144">This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage.</span></span> <span data-ttu-id="e862b-145">Für XML-Dokumente, die nicht in InfoPath erstellt wurden, können einem Tool wie Microsoft Visual Studio zum Erstellen eines Schemas aus dem Beispiel-XML-Dokument oder Sie können das Erstellen eines Beispielformulars aus dem XML-Dokument in InfoPath und exportieren Sie das Schema, das InfoPath von t abgeleitet ist. er Dokumentstruktur.</span><span class="sxs-lookup"><span data-stu-id="e862b-145">For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="e862b-146">Identifizieren Sie die Daten, die Sie über jede Art von XML-Quelldokument zusammenführen möchten.</span><span class="sxs-lookup"><span data-stu-id="e862b-146">Identify the data that you want to merge from each kind of XML source document.</span></span> <span data-ttu-id="e862b-147">Dieser Schritt ist nahezu vollständig die Anforderungen der Quelle und des Ziels Formulare abhängig.</span><span class="sxs-lookup"><span data-stu-id="e862b-147">This step will depend almost entirely on the requirements of both your source and destination forms.</span></span> <span data-ttu-id="e862b-148">Für manche Formulare können Sie alle Daten aus dem Quellformular kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e862b-148">For some forms, you may want to copy all of the data from the source form.</span></span> <span data-ttu-id="e862b-149">Für andere Benutzer sollten Sie nur ein oder zwei Elemente aus dem Formular zugrunde liegenden XML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="e862b-149">For others, you may want only one or two elements from the form's underlying XML document.</span></span> <span data-ttu-id="e862b-150">Beim Festlegen, welche Daten, die Sie zusammenführen möchten, achten Sie zusätzliche auf sowohl die Quell-als auch Dokumente, um sicherzustellen, dass die Elemente logisch zwischen den beiden Formularen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e862b-150">When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="e862b-151">Erstellen Sie eine XSL-Transformation für jede Art von XML-Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="e862b-151">Create an XSL transform for each kind of XML source document.</span></span> <span data-ttu-id="e862b-152">Wenn das Zusammenführen von Formularen konfigurieren, wird dieser Schritt die meiste Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="e862b-152">When configuring the merging of your forms, this step will take the most time.</span></span> <span data-ttu-id="e862b-153">Der Zweck der XSL-Transformation ist das Quell-XML-Dokument in ein Format umgewandelt, die mit dem Zielformular zusammengeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="e862b-153">The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form.</span></span> <span data-ttu-id="e862b-154">Beim Entwerfen Ihrer Transform entscheiden Sie, ob Sie Zusammenführen von XML-Speicherortpfade oder Zusammenführen von InfoPath Aggregation Anweisungen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e862b-154">When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="e862b-155">Visual Studio ist ein praktisches Tool zum Erstellen von XSL-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="e862b-155">Visual Studio is a convenient tool for creating XSL transforms.</span></span> <span data-ttu-id="e862b-156">Visual Studio bietet Syntax Codefarben und ein Dokument Gliederung an.</span><span class="sxs-lookup"><span data-stu-id="e862b-156">Visual Studio provides syntax coloring and a document outline.</span></span> <span data-ttu-id="e862b-157">Es bietet auch automatisch schließenden Tags für XSL-Elemente, die Abnahme redundante Eingaben und schwer zu suchenden Rechtschreibfehler helfen können.</span><span class="sxs-lookup"><span data-stu-id="e862b-157">It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors.</span></span> <span data-ttu-id="e862b-158">Sie können auch die XSL-Transformationen mit einem Text-Editor wie Editor erstellen.</span><span class="sxs-lookup"><span data-stu-id="e862b-158">You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="e862b-159">Beginnen Sie mit der Identitätstransformation, bei der es sich einfach um eine XSL-Transformation handelt, mit der die eingegebene XML-Datei ausgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="e862b-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
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

    <span data-ttu-id="e862b-160">Fügen Sie überschreibende Bereiche der Dokumentvorlage für die Elemente, denen Sie besondere Behandlung für den hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="e862b-160">Then add overriding template sections for the elements you want to add special handling for.</span></span> <span data-ttu-id="e862b-161">Diese Vorlage beispielsweise ändert ein `<src:Task>` Element in einer `<my:field1>` -Element, und legt der Wert des **agg: Action** -Attribut, um "ersetzen".</span><span class="sxs-lookup"><span data-stu-id="e862b-161">For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="e862b-162">Fügen Sie die XSL-Transformationsdateien und Schemadateien in der Formularvorlage ein.</span><span class="sxs-lookup"><span data-stu-id="e862b-162">Add the XSL transform files and schema files in the form template.</span></span> <span data-ttu-id="e862b-163">Nach-Schemas für jede Art von Quelldokument abgeleitet und erstellt eine XSL-Transformation zum Konvertieren jedes Dokumenttyps, damit die Daten von InfoPath zusammengeführt werden kann, fügen sie auf dem Formular als Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="e862b-163">After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form.</span></span> <span data-ttu-id="e862b-164">Klicken Sie auf der Registerkarte **Daten** auf **Ressourcendateien** und klicken Sie dann auf **Hinzufügen** , klicken Sie im Dialogfeld **Ressourcendateien** , wechseln Sie zu Ihrem Schema oder XSL-Transformation-Datei, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e862b-164">Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**.</span></span> <span data-ttu-id="e862b-165">Führen Sie diese Option, um für jede Schemadatei und XSL-Transformation-Datei, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e862b-165">Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="e862b-166">Wenn die Schemas, die Sie hinzufügen das **TargetNamespace** -Attribut verwenden, müssen Sie ein Property-Element für das Formular XSF-Datei hinzufügen, sodass InfoPath den Namespace des Schemas kennt.</span><span class="sxs-lookup"><span data-stu-id="e862b-166">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema.</span></span> <span data-ttu-id="e862b-167">Zugriff auf diese Datei, klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Veröffentlichen**, und klicken Sie dann auf **Quelldateien exportieren**.</span><span class="sxs-lookup"><span data-stu-id="e862b-167">To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**.</span></span> <span data-ttu-id="e862b-168">Wählen Sie einen Speicherort für die Dateien, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e862b-168">Select a location for the files, and then click **OK**.</span></span> <span data-ttu-id="e862b-169">Schließen Sie dann die InfoPath-Formularvorlage, die Sie entwerfen.</span><span class="sxs-lookup"><span data-stu-id="e862b-169">Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="e862b-170">Navigieren Sie zum Speicherort, den Sie für die extrahierten Dateien angegeben, und suchen Sie die Datei, die Erweiterung XSF-Datei hat.</span><span class="sxs-lookup"><span data-stu-id="e862b-170">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension.</span></span> <span data-ttu-id="e862b-171">Normalerweise wird diese Datei manifest.xsf bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e862b-171">Usually, this file is called manifest.xsf.</span></span> <span data-ttu-id="e862b-172">Beim Suchen der Datei in Editor öffnen der `<xsf:file>` -Tag, das Ihrem Schema entspricht, und fügen eine "Namespace" Property-Element zum **TargetNamespace** angeben, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e862b-172">Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="e862b-173">Vorbereiten des Formulars zur Unterstützung von benutzerdefinierten Zusammenführung der letzte Schritt besteht darin, **ImportParameters** -Element in der XSF-Datei, die dem Formular zugeordneten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e862b-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="e862b-174">Suchen Sie zunächst die `<xsf:importParameters>` Tag in der XSF-Datei.</span><span class="sxs-lookup"><span data-stu-id="e862b-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="e862b-175">Für jedes Schema-XSL-Transformationspaar Sie für Ihr Formular erstellt haben, fügen Sie **-Element ein** **importSource** -Element: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="e862b-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="e862b-176">**Name** -Attributs **der-Element** enthält die Namen der Formularvorlage, die in einem XML-Quelldokument gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e862b-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="e862b-177">In der Regel können Sie dies leer lassen.</span><span class="sxs-lookup"><span data-stu-id="e862b-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="e862b-178">Das **Schema** -Attribut enthält den Namen einer Schemadatei, die Sie die Formularvorlage im vorherigen Schritt hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="e862b-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="e862b-179">Schließlich enthält das **transform** -Attribut den Namen der XSL-Transformation, die Sie zum Konvertieren von Formularen, die entsprechen dem Schema verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e862b-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="e862b-180">Sie können entweder mit dem [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis oder auf einem eigenen eine benutzerdefinierte Transformation verwenden.</span><span class="sxs-lookup"><span data-stu-id="e862b-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="e862b-181">Erstellen einer benutzerdefinierten Zusammenführung in Code</span><span class="sxs-lookup"><span data-stu-id="e862b-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="e862b-182">Benutzerdefinierte Zusammenführung mit Code wird mithilfe des ereignishandlers [Zusammenführen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) mit seinem entsprechenden **UseScriptHandler** -Attribut des **ImportParameters** -Elements in der XSF-Datei, die dem Formular zugeordneten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e862b-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="e862b-183">In verwaltetem Code können Sie das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis aktivieren, indem das Kontrollkästchen **Mithilfe benutzerdefiniertem Code Zusammenführen**, und dann auf die Schaltfläche **Bearbeiten** in der Kategorie **Erweitert** im Dialogfeld **Formularoptionen** aus der Backstage-Ansicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e862b-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

