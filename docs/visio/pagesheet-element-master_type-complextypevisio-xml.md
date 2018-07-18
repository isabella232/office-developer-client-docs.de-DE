---
title: PageSheet-Element (Master_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797631"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="113cd-103">PageSheet-Element (Master_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="113cd-103">PageSheet element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="113cd-104">Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="113cd-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="113cd-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="113cd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="113cd-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="113cd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="113cd-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="113cd-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="113cd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="113cd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="113cd-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="113cd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="113cd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="113cd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="113cd-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="113cd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="113cd-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="113cd-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="113cd-113">Definition</span><span class="sxs-lookup"><span data-stu-id="113cd-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="113cd-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="113cd-114">Elements and attributes</span></span>

<span data-ttu-id="113cd-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="113cd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="113cd-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="113cd-116">Parent elements</span></span>

|<span data-ttu-id="113cd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="113cd-117">**Element**</span></span>|<span data-ttu-id="113cd-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="113cd-118">**Type**</span></span>|<span data-ttu-id="113cd-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="113cd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="113cd-120">Master</span><span class="sxs-lookup"><span data-stu-id="113cd-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="113cd-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="113cd-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="113cd-122">Gibt ein Master-Shape in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="113cd-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="113cd-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="113cd-123">Child elements</span></span>

<span data-ttu-id="113cd-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="113cd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="113cd-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="113cd-125">Attributes</span></span>

|<span data-ttu-id="113cd-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="113cd-126">**Attribute**</span></span>|<span data-ttu-id="113cd-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="113cd-127">**Type**</span></span>|<span data-ttu-id="113cd-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="113cd-128">**Required**</span></span>|<span data-ttu-id="113cd-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="113cd-129">**Description**</span></span>|<span data-ttu-id="113cd-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="113cd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="113cd-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="113cd-131">FillStyle</span></span>  <br/> |<span data-ttu-id="113cd-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="113cd-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="113cd-133">Optional</span><span class="sxs-lookup"><span data-stu-id="113cd-133">optional</span></span>  <br/> |<span data-ttu-id="113cd-134">Gibt die ID des Stylesheets von der Füllung Formatierung geerbt.</span><span class="sxs-lookup"><span data-stu-id="113cd-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="113cd-135">Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="113cd-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="113cd-136">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="113cd-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="113cd-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="113cd-137">LineStyle</span></span>  <br/> |<span data-ttu-id="113cd-138">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="113cd-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="113cd-139">Optional</span><span class="sxs-lookup"><span data-stu-id="113cd-139">optional</span></span>  <br/> |<span data-ttu-id="113cd-140">Gibt die ID des Stylesheets von der linienformatierung geerbt.</span><span class="sxs-lookup"><span data-stu-id="113cd-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="113cd-141">Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="113cd-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="113cd-142">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="113cd-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="113cd-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="113cd-143">TextStyle</span></span>  <br/> |<span data-ttu-id="113cd-144">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="113cd-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="113cd-145">Optional</span><span class="sxs-lookup"><span data-stu-id="113cd-145">optional</span></span>  <br/> |<span data-ttu-id="113cd-146">Gibt die ID des Stylesheets aus dem Text-Formatierung erben.</span><span class="sxs-lookup"><span data-stu-id="113cd-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="113cd-147">Es muss der Wert des **ID** -Attributs einen **StyleSheet_Type** in der Zeichnung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="113cd-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="113cd-148">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="113cd-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="113cd-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="113cd-149">UniqueID</span></span>  <br/> |<span data-ttu-id="113cd-150">XSD: String</span><span class="sxs-lookup"><span data-stu-id="113cd-150">xsd:string</span></span>  <br/> |<span data-ttu-id="113cd-151">Optional</span><span class="sxs-lookup"><span data-stu-id="113cd-151">optional</span></span>  <br/> |<span data-ttu-id="113cd-152">Die eindeutige ID des Elements in seinem übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="113cd-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="113cd-153">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="113cd-153">Values of the xsd:string type.</span></span>  <br/> |
   

