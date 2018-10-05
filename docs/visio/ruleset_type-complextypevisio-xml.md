---
title: RuleSet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393621"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="d1e53-102">RuleSet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d1e53-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d1e53-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d1e53-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1e53-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d1e53-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d1e53-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d1e53-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d1e53-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d1e53-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d1e53-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d1e53-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d1e53-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d1e53-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d1e53-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d1e53-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d1e53-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d1e53-110">Elements and attributes</span></span>

<span data-ttu-id="d1e53-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d1e53-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d1e53-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1e53-112">Child elements</span></span>

|<span data-ttu-id="d1e53-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1e53-113">**Element**</span></span>|<span data-ttu-id="d1e53-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d1e53-114">**Type**</span></span>|<span data-ttu-id="d1e53-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1e53-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d1e53-116">Rule</span><span class="sxs-lookup"><span data-stu-id="d1e53-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d1e53-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="d1e53-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d1e53-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="d1e53-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d1e53-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="d1e53-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d1e53-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1e53-120">Attributes</span></span>

|<span data-ttu-id="d1e53-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d1e53-121">**Attribute**</span></span>|<span data-ttu-id="d1e53-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d1e53-122">**Type**</span></span>|<span data-ttu-id="d1e53-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d1e53-123">**Required**</span></span>|<span data-ttu-id="d1e53-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1e53-124">**Description**</span></span>|<span data-ttu-id="d1e53-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d1e53-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d1e53-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1e53-126">Description</span></span>  <br/> |<span data-ttu-id="d1e53-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d1e53-127">xsd:string</span></span>  <br/> |<span data-ttu-id="d1e53-128">Optional</span><span class="sxs-lookup"><span data-stu-id="d1e53-128">optional</span></span>  <br/> ||<span data-ttu-id="d1e53-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d1e53-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d1e53-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d1e53-130">Enabled</span></span>  <br/> |<span data-ttu-id="d1e53-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d1e53-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d1e53-132">Optional</span><span class="sxs-lookup"><span data-stu-id="d1e53-132">optional</span></span>  <br/> ||<span data-ttu-id="d1e53-133">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="d1e53-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d1e53-134">ID</span><span class="sxs-lookup"><span data-stu-id="d1e53-134">ID</span></span>  <br/> |<span data-ttu-id="d1e53-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d1e53-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d1e53-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d1e53-136">required</span></span>  <br/> ||<span data-ttu-id="d1e53-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d1e53-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d1e53-138">Name</span><span class="sxs-lookup"><span data-stu-id="d1e53-138">Name</span></span>  <br/> |<span data-ttu-id="d1e53-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d1e53-139">xsd:string</span></span>  <br/> |<span data-ttu-id="d1e53-140">Optional</span><span class="sxs-lookup"><span data-stu-id="d1e53-140">optional</span></span>  <br/> ||<span data-ttu-id="d1e53-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d1e53-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d1e53-142">NameU</span><span class="sxs-lookup"><span data-stu-id="d1e53-142">NameU</span></span>  <br/> |<span data-ttu-id="d1e53-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d1e53-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d1e53-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d1e53-144">required</span></span>  <br/> ||<span data-ttu-id="d1e53-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d1e53-145">Values of the xsd:string type.</span></span>  <br/> |
   

