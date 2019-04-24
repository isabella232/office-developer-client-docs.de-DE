---
title: RuleSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307742"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="7927d-102">RuleSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7927d-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7927d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7927d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7927d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7927d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7927d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7927d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7927d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7927d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7927d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7927d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7927d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7927d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7927d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7927d-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7927d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7927d-110">Elements and attributes</span></span>

<span data-ttu-id="7927d-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7927d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7927d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7927d-112">Child elements</span></span>

|<span data-ttu-id="7927d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7927d-113">**Element**</span></span>|<span data-ttu-id="7927d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7927d-114">**Type**</span></span>|<span data-ttu-id="7927d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7927d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7927d-116">Rule</span><span class="sxs-lookup"><span data-stu-id="7927d-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7927d-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="7927d-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7927d-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="7927d-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7927d-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="7927d-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7927d-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="7927d-120">Attributes</span></span>

|<span data-ttu-id="7927d-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7927d-121">**Attribute**</span></span>|<span data-ttu-id="7927d-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7927d-122">**Type**</span></span>|<span data-ttu-id="7927d-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7927d-123">**Required**</span></span>|<span data-ttu-id="7927d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7927d-124">**Description**</span></span>|<span data-ttu-id="7927d-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7927d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7927d-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7927d-126">Description</span></span>  <br/> |<span data-ttu-id="7927d-127">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7927d-127">xsd:string</span></span>  <br/> |<span data-ttu-id="7927d-128">Optional</span><span class="sxs-lookup"><span data-stu-id="7927d-128">optional</span></span>  <br/> ||<span data-ttu-id="7927d-129">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7927d-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7927d-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="7927d-130">Enabled</span></span>  <br/> |<span data-ttu-id="7927d-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7927d-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7927d-132">Optional</span><span class="sxs-lookup"><span data-stu-id="7927d-132">optional</span></span>  <br/> ||<span data-ttu-id="7927d-133">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="7927d-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7927d-134">ID</span><span class="sxs-lookup"><span data-stu-id="7927d-134">ID</span></span>  <br/> |<span data-ttu-id="7927d-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7927d-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7927d-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7927d-136">required</span></span>  <br/> ||<span data-ttu-id="7927d-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="7927d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7927d-138">Name</span><span class="sxs-lookup"><span data-stu-id="7927d-138">Name</span></span>  <br/> |<span data-ttu-id="7927d-139">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7927d-139">xsd:string</span></span>  <br/> |<span data-ttu-id="7927d-140">Optional</span><span class="sxs-lookup"><span data-stu-id="7927d-140">optional</span></span>  <br/> ||<span data-ttu-id="7927d-141">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7927d-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7927d-142">NameU</span><span class="sxs-lookup"><span data-stu-id="7927d-142">NameU</span></span>  <br/> |<span data-ttu-id="7927d-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7927d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="7927d-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7927d-144">required</span></span>  <br/> ||<span data-ttu-id="7927d-145">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="7927d-145">Values of the xsd:string type.</span></span>  <br/> |
   

