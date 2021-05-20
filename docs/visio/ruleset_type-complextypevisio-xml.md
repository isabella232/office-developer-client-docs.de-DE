---
title: RuleSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 5d3d29ee7ae48c344afcdce3faf5e26d5f564501
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541624"
---
# <a name="ruleset_type-complextype-visio-xml"></a><span data-ttu-id="83ae4-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="83ae4-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="83ae4-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="83ae4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83ae4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="83ae4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="83ae4-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="83ae4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="83ae4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="83ae4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="83ae4-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="83ae4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="83ae4-108">Keine</span><span class="sxs-lookup"><span data-stu-id="83ae4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="83ae4-109">Definition</span><span class="sxs-lookup"><span data-stu-id="83ae4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="83ae4-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="83ae4-110">Elements and attributes</span></span>

<span data-ttu-id="83ae4-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="83ae4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="83ae4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83ae4-112">Child elements</span></span>

|<span data-ttu-id="83ae4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83ae4-113">**Element**</span></span>|<span data-ttu-id="83ae4-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="83ae4-114">**Type**</span></span>|<span data-ttu-id="83ae4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83ae4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="83ae4-116">Rule</span><span class="sxs-lookup"><span data-stu-id="83ae4-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="83ae4-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="83ae4-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="83ae4-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="83ae4-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="83ae4-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="83ae4-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="83ae4-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="83ae4-120">Attributes</span></span>

|<span data-ttu-id="83ae4-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="83ae4-121">**Attribute**</span></span>|<span data-ttu-id="83ae4-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="83ae4-122">**Type**</span></span>|<span data-ttu-id="83ae4-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="83ae4-123">**Required**</span></span>|<span data-ttu-id="83ae4-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83ae4-124">**Description**</span></span>|<span data-ttu-id="83ae4-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="83ae4-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="83ae4-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83ae4-126">Description</span></span>  <br/> |<span data-ttu-id="83ae4-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="83ae4-127">xsd:string</span></span>  <br/> |<span data-ttu-id="83ae4-128">Optional</span><span class="sxs-lookup"><span data-stu-id="83ae4-128">optional</span></span>  <br/> ||<span data-ttu-id="83ae4-129">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="83ae4-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="83ae4-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="83ae4-130">Enabled</span></span>  <br/> |<span data-ttu-id="83ae4-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="83ae4-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="83ae4-132">Optional</span><span class="sxs-lookup"><span data-stu-id="83ae4-132">optional</span></span>  <br/> ||<span data-ttu-id="83ae4-133">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="83ae4-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="83ae4-134">ID</span><span class="sxs-lookup"><span data-stu-id="83ae4-134">ID</span></span>  <br/> |<span data-ttu-id="83ae4-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="83ae4-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="83ae4-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="83ae4-136">required</span></span>  <br/> ||<span data-ttu-id="83ae4-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="83ae4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="83ae4-138">Name</span><span class="sxs-lookup"><span data-stu-id="83ae4-138">Name</span></span>  <br/> |<span data-ttu-id="83ae4-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="83ae4-139">xsd:string</span></span>  <br/> |<span data-ttu-id="83ae4-140">Optional</span><span class="sxs-lookup"><span data-stu-id="83ae4-140">optional</span></span>  <br/> ||<span data-ttu-id="83ae4-141">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="83ae4-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="83ae4-142">NameU</span><span class="sxs-lookup"><span data-stu-id="83ae4-142">NameU</span></span>  <br/> |<span data-ttu-id="83ae4-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="83ae4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="83ae4-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="83ae4-144">required</span></span>  <br/> ||<span data-ttu-id="83ae4-145">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="83ae4-145">Values of the xsd:string type.</span></span>  <br/> |
   

