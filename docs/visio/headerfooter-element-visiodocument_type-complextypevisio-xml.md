---
title: HeaderFooter-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541106"
---
# <a name="headerfooter-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="01b5c-103">HeaderFooter-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="01b5c-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="01b5c-104">Enthält Elemente für die Kopf- und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="01b5c-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01b5c-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="01b5c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01b5c-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="01b5c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="01b5c-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="01b5c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="01b5c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="01b5c-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="01b5c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="01b5c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="01b5c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="01b5c-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="01b5c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="01b5c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="01b5c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01b5c-113">Definition</span><span class="sxs-lookup"><span data-stu-id="01b5c-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="01b5c-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="01b5c-114">Elements and attributes</span></span>

<span data-ttu-id="01b5c-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="01b5c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="01b5c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01b5c-116">Parent elements</span></span>

|<span data-ttu-id="01b5c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="01b5c-117">**Element**</span></span>|<span data-ttu-id="01b5c-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="01b5c-118">**Type**</span></span>|<span data-ttu-id="01b5c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01b5c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01b5c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="01b5c-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="01b5c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-122">Das Stammelement eines Microsoft-Visio Dokument.</span><span class="sxs-lookup"><span data-stu-id="01b5c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01b5c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01b5c-123">Child elements</span></span>

|<span data-ttu-id="01b5c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="01b5c-124">**Element**</span></span>|<span data-ttu-id="01b5c-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="01b5c-125">**Type**</span></span>|<span data-ttu-id="01b5c-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01b5c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01b5c-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="01b5c-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-129">Enthält die Textzeichenfolge, die im Mittelpunkt der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="01b5c-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-132">Enthält die Textzeichenfolge, die im linken Teil der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="01b5c-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-135">Gibt den Rand der Fußzeile eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="01b5c-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="01b5c-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-138">Enthält die Textzeichenfolge, die im rechten Teil der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="01b5c-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-141">Enthält die Textzeichenfolge, die im mittleren Bereich der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="01b5c-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-144">Gibt die Schriftart an, die für den Text in der Kopf- und Fußzeile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="01b5c-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-147">Enthält die Textzeichenfolge, die im linken Teil der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="01b5c-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-150">Gibt den Rand der Kopfzeile eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="01b5c-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="01b5c-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="01b5c-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b5c-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="01b5c-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b5c-153">Enthält die Textzeichenfolge, die im rechten Teil der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01b5c-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="01b5c-154">Attribute</span><span class="sxs-lookup"><span data-stu-id="01b5c-154">Attributes</span></span>

|<span data-ttu-id="01b5c-155">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="01b5c-155">**Attribute**</span></span>|<span data-ttu-id="01b5c-156">**Typ**</span><span class="sxs-lookup"><span data-stu-id="01b5c-156">**Type**</span></span>|<span data-ttu-id="01b5c-157">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="01b5c-157">**Required**</span></span>|<span data-ttu-id="01b5c-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01b5c-158">**Description**</span></span>|<span data-ttu-id="01b5c-159">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="01b5c-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01b5c-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="01b5c-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="01b5c-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="01b5c-161">xsd:string</span></span>  <br/> |<span data-ttu-id="01b5c-162">Optional</span><span class="sxs-lookup"><span data-stu-id="01b5c-162">optional</span></span>  <br/> |<span data-ttu-id="01b5c-163">Der #A0 der Textfarbe für die Kopf- und Fußzeile in hexadezimaler Notation; Beispiel: #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="01b5c-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="01b5c-164">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="01b5c-164">Values of the xsd:string type.</span></span>  <br/> |
   

