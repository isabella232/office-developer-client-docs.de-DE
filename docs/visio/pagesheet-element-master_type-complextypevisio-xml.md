---
title: PageSheet-Element (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540616"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a><span data-ttu-id="68234-103">PageSheet-Element (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="68234-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="68234-104">Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68234-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68234-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68234-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68234-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="68234-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68234-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="68234-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68234-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68234-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68234-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="68234-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68234-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="68234-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68234-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="68234-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68234-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="68234-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68234-113">Definition</span><span class="sxs-lookup"><span data-stu-id="68234-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68234-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="68234-114">Elements and attributes</span></span>

<span data-ttu-id="68234-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="68234-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68234-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68234-116">Parent elements</span></span>

|<span data-ttu-id="68234-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="68234-117">**Element**</span></span>|<span data-ttu-id="68234-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68234-118">**Type**</span></span>|<span data-ttu-id="68234-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68234-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68234-120">Master</span><span class="sxs-lookup"><span data-stu-id="68234-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68234-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="68234-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68234-122">Gibt einen Master in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="68234-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68234-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68234-123">Child elements</span></span>

<span data-ttu-id="68234-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="68234-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68234-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="68234-125">Attributes</span></span>

|<span data-ttu-id="68234-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68234-126">**Attribute**</span></span>|<span data-ttu-id="68234-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68234-127">**Type**</span></span>|<span data-ttu-id="68234-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="68234-128">**Required**</span></span>|<span data-ttu-id="68234-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68234-129">**Description**</span></span>|<span data-ttu-id="68234-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="68234-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68234-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="68234-131">FillStyle</span></span>  <br/> |<span data-ttu-id="68234-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68234-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68234-133">Optional</span><span class="sxs-lookup"><span data-stu-id="68234-133">optional</span></span>  <br/> |<span data-ttu-id="68234-134">gibt die ID des Stylesheets an, von dem die Füllformatierung erben werden soll.</span><span class="sxs-lookup"><span data-stu-id="68234-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="68234-135">Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68234-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="68234-136">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="68234-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68234-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="68234-137">LineStyle</span></span>  <br/> |<span data-ttu-id="68234-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68234-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68234-139">Optional</span><span class="sxs-lookup"><span data-stu-id="68234-139">optional</span></span>  <br/> |<span data-ttu-id="68234-140">Gibt die ID des Stylesheets an, von dem zeilenformatiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="68234-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="68234-141">Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68234-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="68234-142">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="68234-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68234-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="68234-143">TextStyle</span></span>  <br/> |<span data-ttu-id="68234-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68234-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68234-145">Optional</span><span class="sxs-lookup"><span data-stu-id="68234-145">optional</span></span>  <br/> |<span data-ttu-id="68234-146">Gibt die ID des Stylesheets an, von dem die Textformatierung erben werden soll.</span><span class="sxs-lookup"><span data-stu-id="68234-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="68234-147">Dies muss der  Wert des ID-Attributs sein, das einem StyleSheet_Type **in** der Zeichnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68234-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="68234-148">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="68234-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68234-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="68234-149">UniqueID</span></span>  <br/> |<span data-ttu-id="68234-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="68234-150">xsd:string</span></span>  <br/> |<span data-ttu-id="68234-151">Optional</span><span class="sxs-lookup"><span data-stu-id="68234-151">optional</span></span>  <br/> |<span data-ttu-id="68234-152">Die eindeutige ID des Elements innerhalb des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="68234-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="68234-153">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="68234-153">Values of the xsd:string type.</span></span>  <br/> |
   

