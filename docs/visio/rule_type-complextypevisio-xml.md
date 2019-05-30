---
title: Rule_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541715"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="ad73d-102">Rule_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ad73d-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ad73d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ad73d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad73d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad73d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad73d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ad73d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad73d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ad73d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad73d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ad73d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad73d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ad73d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad73d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ad73d-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad73d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ad73d-110">Elements and attributes</span></span>

<span data-ttu-id="ad73d-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ad73d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad73d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad73d-112">Child elements</span></span>

|<span data-ttu-id="ad73d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad73d-113">**Element**</span></span>|<span data-ttu-id="ad73d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad73d-114">**Type**</span></span>|<span data-ttu-id="ad73d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad73d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad73d-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="ad73d-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad73d-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="ad73d-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad73d-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="ad73d-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad73d-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="ad73d-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad73d-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad73d-120">Attributes</span></span>

|<span data-ttu-id="ad73d-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad73d-121">**Attribute**</span></span>|<span data-ttu-id="ad73d-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad73d-122">**Type**</span></span>|<span data-ttu-id="ad73d-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ad73d-123">**Required**</span></span>|<span data-ttu-id="ad73d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad73d-124">**Description**</span></span>|<span data-ttu-id="ad73d-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ad73d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad73d-126">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ad73d-126">Category</span></span>  <br/> |<span data-ttu-id="ad73d-127">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad73d-127">xsd:string</span></span>  <br/> |<span data-ttu-id="ad73d-128">Optional</span><span class="sxs-lookup"><span data-stu-id="ad73d-128">optional</span></span>  <br/> ||<span data-ttu-id="ad73d-129">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ad73d-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad73d-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad73d-130">Description</span></span>  <br/> |<span data-ttu-id="ad73d-131">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad73d-131">xsd:string</span></span>  <br/> |<span data-ttu-id="ad73d-132">Optional</span><span class="sxs-lookup"><span data-stu-id="ad73d-132">optional</span></span>  <br/> ||<span data-ttu-id="ad73d-133">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ad73d-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad73d-134">ID</span><span class="sxs-lookup"><span data-stu-id="ad73d-134">ID</span></span>  <br/> |<span data-ttu-id="ad73d-135">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad73d-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad73d-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad73d-136">required</span></span>  <br/> ||<span data-ttu-id="ad73d-137">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ad73d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad73d-138">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="ad73d-138">Ignored</span></span>  <br/> |<span data-ttu-id="ad73d-139">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ad73d-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad73d-140">Optional</span><span class="sxs-lookup"><span data-stu-id="ad73d-140">optional</span></span>  <br/> ||<span data-ttu-id="ad73d-141">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ad73d-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad73d-142">NameU</span><span class="sxs-lookup"><span data-stu-id="ad73d-142">NameU</span></span>  <br/> |<span data-ttu-id="ad73d-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad73d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ad73d-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad73d-144">required</span></span>  <br/> ||<span data-ttu-id="ad73d-145">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ad73d-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad73d-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="ad73d-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="ad73d-147">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ad73d-147">xsd:int</span></span>  <br/> |<span data-ttu-id="ad73d-148">Optional</span><span class="sxs-lookup"><span data-stu-id="ad73d-148">optional</span></span>  <br/> ||<span data-ttu-id="ad73d-149">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="ad73d-149">Values of the xsd:int type.</span></span>  <br/> |
   

