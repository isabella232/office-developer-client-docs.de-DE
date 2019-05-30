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
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="bf480-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bf480-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bf480-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bf480-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf480-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bf480-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bf480-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bf480-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bf480-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="bf480-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bf480-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bf480-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bf480-108">Keine</span><span class="sxs-lookup"><span data-stu-id="bf480-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf480-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bf480-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bf480-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bf480-110">Elements and attributes</span></span>

<span data-ttu-id="bf480-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="bf480-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bf480-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf480-112">Child elements</span></span>

|<span data-ttu-id="bf480-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf480-113">**Element**</span></span>|<span data-ttu-id="bf480-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bf480-114">**Type**</span></span>|<span data-ttu-id="bf480-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf480-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf480-116">Rule</span><span class="sxs-lookup"><span data-stu-id="bf480-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf480-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="bf480-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf480-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="bf480-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf480-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="bf480-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bf480-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="bf480-120">Attributes</span></span>

|<span data-ttu-id="bf480-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bf480-121">**Attribute**</span></span>|<span data-ttu-id="bf480-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bf480-122">**Type**</span></span>|<span data-ttu-id="bf480-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bf480-123">**Required**</span></span>|<span data-ttu-id="bf480-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf480-124">**Description**</span></span>|<span data-ttu-id="bf480-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bf480-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf480-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf480-126">Description</span></span>  <br/> |<span data-ttu-id="bf480-127">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf480-127">xsd:string</span></span>  <br/> |<span data-ttu-id="bf480-128">Optional</span><span class="sxs-lookup"><span data-stu-id="bf480-128">optional</span></span>  <br/> ||<span data-ttu-id="bf480-129">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bf480-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bf480-130">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="bf480-130">Enabled</span></span>  <br/> |<span data-ttu-id="bf480-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bf480-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bf480-132">Optional</span><span class="sxs-lookup"><span data-stu-id="bf480-132">optional</span></span>  <br/> ||<span data-ttu-id="bf480-133">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="bf480-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bf480-134">ID</span><span class="sxs-lookup"><span data-stu-id="bf480-134">ID</span></span>  <br/> |<span data-ttu-id="bf480-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bf480-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf480-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf480-136">required</span></span>  <br/> ||<span data-ttu-id="bf480-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="bf480-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bf480-138">Name</span><span class="sxs-lookup"><span data-stu-id="bf480-138">Name</span></span>  <br/> |<span data-ttu-id="bf480-139">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf480-139">xsd:string</span></span>  <br/> |<span data-ttu-id="bf480-140">Optional</span><span class="sxs-lookup"><span data-stu-id="bf480-140">optional</span></span>  <br/> ||<span data-ttu-id="bf480-141">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bf480-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bf480-142">NameU</span><span class="sxs-lookup"><span data-stu-id="bf480-142">NameU</span></span>  <br/> |<span data-ttu-id="bf480-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bf480-143">xsd:string</span></span>  <br/> |<span data-ttu-id="bf480-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf480-144">required</span></span>  <br/> ||<span data-ttu-id="bf480-145">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bf480-145">Values of the xsd:string type.</span></span>  <br/> |
   

