---
title: Row_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: ebd3b666590e6144d2a3cb6e0059b64eb6e8dab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2019
ms.locfileid: "32331647"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="c1b15-102">Row_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c1b15-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c1b15-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c1b15-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1b15-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1b15-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c1b15-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c1b15-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c1b15-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c1b15-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c1b15-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c1b15-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c1b15-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c1b15-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1b15-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c1b15-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1b15-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c1b15-110">Elements and attributes</span></span>

<span data-ttu-id="c1b15-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c1b15-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c1b15-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1b15-112">Child elements</span></span>

|<span data-ttu-id="c1b15-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1b15-113">**Element**</span></span>|<span data-ttu-id="c1b15-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c1b15-114">**Type**</span></span>|<span data-ttu-id="c1b15-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1b15-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1b15-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c1b15-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="c1b15-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c1b15-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c1b15-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="c1b15-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="c1b15-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c1b15-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c1b15-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1b15-120">Attributes</span></span>

|<span data-ttu-id="c1b15-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1b15-121">**Attribute**</span></span>|<span data-ttu-id="c1b15-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c1b15-122">**Type**</span></span>|<span data-ttu-id="c1b15-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c1b15-123">**Required**</span></span>|<span data-ttu-id="c1b15-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1b15-124">**Description**</span></span>|<span data-ttu-id="c1b15-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c1b15-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1b15-126">ENTF</span><span class="sxs-lookup"><span data-stu-id="c1b15-126">Del</span></span>  <br/> |<span data-ttu-id="c1b15-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b15-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c1b15-128">Optional</span><span class="sxs-lookup"><span data-stu-id="c1b15-128">optional</span></span>  <br/> ||<span data-ttu-id="c1b15-129">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c1b15-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c1b15-130">IX</span><span class="sxs-lookup"><span data-stu-id="c1b15-130">IX</span></span>  <br/> |<span data-ttu-id="c1b15-131">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c1b15-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1b15-132">Optional</span><span class="sxs-lookup"><span data-stu-id="c1b15-132">optional</span></span>  <br/> ||<span data-ttu-id="c1b15-133">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c1b15-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c1b15-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="c1b15-134">LocalName</span></span>  <br/> |<span data-ttu-id="c1b15-135">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1b15-135">xsd:string</span></span>  <br/> |<span data-ttu-id="c1b15-136">Optional</span><span class="sxs-lookup"><span data-stu-id="c1b15-136">optional</span></span>  <br/> ||<span data-ttu-id="c1b15-137">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="c1b15-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1b15-138">N</span><span class="sxs-lookup"><span data-stu-id="c1b15-138">N</span></span>  <br/> |<span data-ttu-id="c1b15-139">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1b15-139">xsd:string</span></span>  <br/> |<span data-ttu-id="c1b15-140">Optional</span><span class="sxs-lookup"><span data-stu-id="c1b15-140">optional</span></span>  <br/> ||<span data-ttu-id="c1b15-141">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="c1b15-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1b15-142">T</span><span class="sxs-lookup"><span data-stu-id="c1b15-142">T</span></span>  <br/> |<span data-ttu-id="c1b15-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c1b15-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c1b15-144">Optional</span><span class="sxs-lookup"><span data-stu-id="c1b15-144">optional</span></span>  <br/> ||<span data-ttu-id="c1b15-145">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="c1b15-145">Values of the xsd:string type.</span></span>  <br/> |
   

