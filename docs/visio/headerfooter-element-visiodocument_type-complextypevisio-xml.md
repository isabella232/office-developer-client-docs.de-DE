---
title: HeaderFooter-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Enthält Elemente für die Kopf-und Fußzeile eines Dokuments.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541106"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="46902-103">HeaderFooter-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="46902-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="46902-104">Enthält Elemente für die Kopf-und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="46902-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46902-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="46902-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46902-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="46902-106">**Element type**</span></span> <br/> |[<span data-ttu-id="46902-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="46902-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="46902-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="46902-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="46902-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="46902-109">**Schema file**</span></span> <br/> |<span data-ttu-id="46902-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="46902-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="46902-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="46902-111">**Document parts**</span></span> <br/> |<span data-ttu-id="46902-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="46902-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46902-113">Definition</span><span class="sxs-lookup"><span data-stu-id="46902-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46902-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="46902-114">Elements and attributes</span></span>

<span data-ttu-id="46902-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="46902-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="46902-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46902-116">Parent elements</span></span>

|<span data-ttu-id="46902-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="46902-117">**Element**</span></span>|<span data-ttu-id="46902-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="46902-118">**Type**</span></span>|<span data-ttu-id="46902-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46902-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46902-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="46902-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="46902-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="46902-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="46902-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="46902-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46902-123">Child elements</span></span>

|<span data-ttu-id="46902-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="46902-124">**Element**</span></span>|<span data-ttu-id="46902-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="46902-125">**Type**</span></span>|<span data-ttu-id="46902-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46902-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46902-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="46902-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="46902-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-129">Enthält die Textzeichenfolge, die im mittleren Teil der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="46902-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="46902-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="46902-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-132">Enthält die Textzeichenfolge, die im linken Teil der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="46902-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="46902-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="46902-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-135">Gibt den Rand der Fußzeile eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="46902-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="46902-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="46902-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="46902-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-138">Enthält die Textzeichenfolge, die im rechten Teil der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="46902-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="46902-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="46902-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-141">Enthält die Textzeichenfolge, die im mittleren Bereich der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="46902-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="46902-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="46902-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-144">Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46902-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="46902-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="46902-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="46902-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-147">Enthält die Textzeichenfolge, die im linken Teil der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="46902-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="46902-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="46902-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-150">Gibt den Rand der Kopfzeile eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="46902-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="46902-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="46902-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46902-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="46902-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46902-153">Enthält die Textzeichenfolge, die im rechten Teil der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46902-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="46902-154">Attribute</span><span class="sxs-lookup"><span data-stu-id="46902-154">Attributes</span></span>

|<span data-ttu-id="46902-155">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="46902-155">**Attribute**</span></span>|<span data-ttu-id="46902-156">**Typ**</span><span class="sxs-lookup"><span data-stu-id="46902-156">**Type**</span></span>|<span data-ttu-id="46902-157">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="46902-157">**Required**</span></span>|<span data-ttu-id="46902-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46902-158">**Description**</span></span>|<span data-ttu-id="46902-159">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="46902-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="46902-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="46902-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="46902-161">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="46902-161">xsd:string</span></span>  <br/> |<span data-ttu-id="46902-162">Optional</span><span class="sxs-lookup"><span data-stu-id="46902-162">optional</span></span>  <br/> |<span data-ttu-id="46902-163">Der RGB-Wert der Textfarbe für die Kopf-und Fußzeile in Hexadezimalnotation; Beispiel: #RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="46902-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="46902-164">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="46902-164">Values of the xsd:string type.</span></span>  <br/> |
   

