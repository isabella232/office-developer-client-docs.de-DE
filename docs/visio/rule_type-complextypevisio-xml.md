---
title: Rule_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797945"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="7f6c0-102">Rule_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7f6c0-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7f6c0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7f6c0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f6c0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7f6c0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7f6c0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7f6c0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7f6c0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7f6c0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7f6c0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f6c0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7f6c0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7f6c0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7f6c0-110">Elements and attributes</span></span>

<span data-ttu-id="7f6c0-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f6c0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f6c0-112">Child elements</span></span>

|<span data-ttu-id="7f6c0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-113">**Element**</span></span>|<span data-ttu-id="7f6c0-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-114">**Type**</span></span>|<span data-ttu-id="7f6c0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7f6c0-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="7f6c0-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7f6c0-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="7f6c0-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7f6c0-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="7f6c0-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7f6c0-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="7f6c0-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7f6c0-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f6c0-120">Attributes</span></span>

|<span data-ttu-id="7f6c0-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-121">**Attribute**</span></span>|<span data-ttu-id="7f6c0-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-122">**Type**</span></span>|<span data-ttu-id="7f6c0-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-123">**Required**</span></span>|<span data-ttu-id="7f6c0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-124">**Description**</span></span>|<span data-ttu-id="7f6c0-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7f6c0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f6c0-126">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7f6c0-126">Category</span></span>  <br/> |<span data-ttu-id="7f6c0-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f6c0-127">xsd:string</span></span>  <br/> |<span data-ttu-id="7f6c0-128">Optional</span><span class="sxs-lookup"><span data-stu-id="7f6c0-128">optional</span></span>  <br/> ||<span data-ttu-id="7f6c0-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f6c0-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f6c0-130">Description</span></span>  <br/> |<span data-ttu-id="7f6c0-131">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f6c0-131">xsd:string</span></span>  <br/> |<span data-ttu-id="7f6c0-132">Optional</span><span class="sxs-lookup"><span data-stu-id="7f6c0-132">optional</span></span>  <br/> ||<span data-ttu-id="7f6c0-133">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f6c0-134">ID</span><span class="sxs-lookup"><span data-stu-id="7f6c0-134">ID</span></span>  <br/> |<span data-ttu-id="7f6c0-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7f6c0-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f6c0-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f6c0-136">required</span></span>  <br/> ||<span data-ttu-id="7f6c0-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7f6c0-138">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="7f6c0-138">Ignored</span></span>  <br/> |<span data-ttu-id="7f6c0-139">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7f6c0-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7f6c0-140">Optional</span><span class="sxs-lookup"><span data-stu-id="7f6c0-140">optional</span></span>  <br/> ||<span data-ttu-id="7f6c0-141">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7f6c0-142">NameU</span><span class="sxs-lookup"><span data-stu-id="7f6c0-142">NameU</span></span>  <br/> |<span data-ttu-id="7f6c0-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7f6c0-143">xsd:string</span></span>  <br/> |<span data-ttu-id="7f6c0-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f6c0-144">required</span></span>  <br/> ||<span data-ttu-id="7f6c0-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f6c0-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="7f6c0-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="7f6c0-147">XSD: int</span><span class="sxs-lookup"><span data-stu-id="7f6c0-147">xsd:int</span></span>  <br/> |<span data-ttu-id="7f6c0-148">Optional</span><span class="sxs-lookup"><span data-stu-id="7f6c0-148">optional</span></span>  <br/> ||<span data-ttu-id="7f6c0-149">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="7f6c0-149">Values of the xsd:int type.</span></span>  <br/> |
   

