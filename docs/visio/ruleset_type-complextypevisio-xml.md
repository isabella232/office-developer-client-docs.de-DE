---
title: RuleSet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797958"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="13890-102">RuleSet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="13890-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="13890-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="13890-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13890-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13890-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="13890-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="13890-105">**Schema file**</span></span> <br/> |<span data-ttu-id="13890-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="13890-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="13890-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="13890-107">**Extension base**</span></span> <br/> |<span data-ttu-id="13890-108">Keine</span><span class="sxs-lookup"><span data-stu-id="13890-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13890-109">Definition</span><span class="sxs-lookup"><span data-stu-id="13890-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="13890-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="13890-110">Elements and attributes</span></span>

<span data-ttu-id="13890-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="13890-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="13890-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13890-112">Child elements</span></span>

|<span data-ttu-id="13890-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="13890-113">**Element**</span></span>|<span data-ttu-id="13890-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="13890-114">**Type**</span></span>|<span data-ttu-id="13890-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13890-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13890-116">Rule</span><span class="sxs-lookup"><span data-stu-id="13890-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13890-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="13890-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13890-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="13890-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13890-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="13890-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="13890-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="13890-120">Attributes</span></span>

|<span data-ttu-id="13890-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="13890-121">**Attribute**</span></span>|<span data-ttu-id="13890-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="13890-122">**Type**</span></span>|<span data-ttu-id="13890-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="13890-123">**Required**</span></span>|<span data-ttu-id="13890-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13890-124">**Description**</span></span>|<span data-ttu-id="13890-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="13890-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13890-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13890-126">Description</span></span>  <br/> |<span data-ttu-id="13890-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="13890-127">xsd:string</span></span>  <br/> |<span data-ttu-id="13890-128">Optional</span><span class="sxs-lookup"><span data-stu-id="13890-128">optional</span></span>  <br/> ||<span data-ttu-id="13890-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="13890-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13890-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="13890-130">Enabled</span></span>  <br/> |<span data-ttu-id="13890-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="13890-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13890-132">Optional</span><span class="sxs-lookup"><span data-stu-id="13890-132">optional</span></span>  <br/> ||<span data-ttu-id="13890-133">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="13890-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13890-134">ID</span><span class="sxs-lookup"><span data-stu-id="13890-134">ID</span></span>  <br/> |<span data-ttu-id="13890-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13890-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13890-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="13890-136">required</span></span>  <br/> ||<span data-ttu-id="13890-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13890-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13890-138">Name</span><span class="sxs-lookup"><span data-stu-id="13890-138">Name</span></span>  <br/> |<span data-ttu-id="13890-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="13890-139">xsd:string</span></span>  <br/> |<span data-ttu-id="13890-140">Optional</span><span class="sxs-lookup"><span data-stu-id="13890-140">optional</span></span>  <br/> ||<span data-ttu-id="13890-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="13890-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13890-142">NameU</span><span class="sxs-lookup"><span data-stu-id="13890-142">NameU</span></span>  <br/> |<span data-ttu-id="13890-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="13890-143">xsd:string</span></span>  <br/> |<span data-ttu-id="13890-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="13890-144">required</span></span>  <br/> ||<span data-ttu-id="13890-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="13890-145">Values of the xsd:string type.</span></span>  <br/> |
   

