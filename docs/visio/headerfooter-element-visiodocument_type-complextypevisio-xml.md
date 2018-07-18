---
title: HeaderFooter-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Enthält Elemente für Kopf- und Fußzeile eines Dokuments.
ms.openlocfilehash: e5933ad318b8100569046668e3cc372ce9a03788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797144"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="4f491-103">HeaderFooter-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4f491-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4f491-104">Enthält Elemente für Kopf- und Fußzeile eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4f491-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f491-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4f491-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f491-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4f491-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f491-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f491-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f491-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f491-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4f491-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f491-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4f491-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f491-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="4f491-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4f491-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="4f491-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f491-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4f491-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f491-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4f491-114">Elements and attributes</span></span>

<span data-ttu-id="4f491-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4f491-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f491-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f491-116">Parent elements</span></span>

|<span data-ttu-id="4f491-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f491-117">**Element**</span></span>|<span data-ttu-id="4f491-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f491-118">**Type**</span></span>|<span data-ttu-id="4f491-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f491-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f491-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4f491-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f491-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4f491-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f491-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f491-123">Child elements</span></span>

|<span data-ttu-id="4f491-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f491-124">**Element**</span></span>|<span data-ttu-id="4f491-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f491-125">**Type**</span></span>|<span data-ttu-id="4f491-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f491-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f491-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="4f491-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-129">Enthält die Textzeichenfolge, die in der Mitte der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="4f491-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="4f491-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-132">Enthält die Textzeichenfolge, die im linken Bereich der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="4f491-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="4f491-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-135">Gibt den Rand der Fußzeile eines Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="4f491-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="4f491-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="4f491-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-138">Enthält die Textzeichenfolge, die im rechten Bereich der Fußzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="4f491-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="4f491-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-141">Enthält die Textzeichenfolge, die im mittleren Bereich der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="4f491-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="4f491-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-144">Gibt die Schriftart für den Text Kopf- und Fußzeile verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f491-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="4f491-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="4f491-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-147">Enthält die Textzeichenfolge, die im linken Bereich der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="4f491-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="4f491-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-150">Gibt den Rand der Kopfzeile des Dokuments an.</span><span class="sxs-lookup"><span data-stu-id="4f491-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="4f491-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="4f491-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f491-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="4f491-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f491-153">Enthält die Textzeichenfolge, die im rechten Bereich der Kopfzeile eines Dokuments angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f491-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f491-154">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f491-154">Attributes</span></span>

|<span data-ttu-id="4f491-155">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f491-155">**Attribute**</span></span>|<span data-ttu-id="4f491-156">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f491-156">**Type**</span></span>|<span data-ttu-id="4f491-157">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4f491-157">**Required**</span></span>|<span data-ttu-id="4f491-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f491-158">**Description**</span></span>|<span data-ttu-id="4f491-159">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4f491-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f491-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="4f491-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="4f491-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4f491-161">xsd:string</span></span>  <br/> |<span data-ttu-id="4f491-162">Optional</span><span class="sxs-lookup"><span data-stu-id="4f491-162">optional</span></span>  <br/> |<span data-ttu-id="4f491-163">Der RGB-Wert der Textfarbe für die Kopf- und Fußzeile in hexadezimaler Schreibweise; beispielsweise #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="4f491-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="4f491-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4f491-164">Values of the xsd:string type.</span></span>  <br/> |
   

