---
title: Rule_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393509"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="3c98a-102">Rule_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3c98a-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3c98a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="3c98a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c98a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3c98a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3c98a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3c98a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3c98a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3c98a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3c98a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="3c98a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3c98a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="3c98a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c98a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="3c98a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3c98a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3c98a-110">Elements and attributes</span></span>

<span data-ttu-id="3c98a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3c98a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3c98a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c98a-112">Child elements</span></span>

|<span data-ttu-id="3c98a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c98a-113">**Element**</span></span>|<span data-ttu-id="3c98a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3c98a-114">**Type**</span></span>|<span data-ttu-id="3c98a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c98a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c98a-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="3c98a-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c98a-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="3c98a-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3c98a-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="3c98a-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c98a-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="3c98a-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3c98a-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c98a-120">Attributes</span></span>

|<span data-ttu-id="3c98a-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3c98a-121">**Attribute**</span></span>|<span data-ttu-id="3c98a-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3c98a-122">**Type**</span></span>|<span data-ttu-id="3c98a-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3c98a-123">**Required**</span></span>|<span data-ttu-id="3c98a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c98a-124">**Description**</span></span>|<span data-ttu-id="3c98a-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3c98a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c98a-126">Kategorie</span><span class="sxs-lookup"><span data-stu-id="3c98a-126">Category</span></span>  <br/> |<span data-ttu-id="3c98a-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3c98a-127">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98a-128">Optional</span><span class="sxs-lookup"><span data-stu-id="3c98a-128">optional</span></span>  <br/> ||<span data-ttu-id="3c98a-129">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3c98a-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98a-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c98a-130">Description</span></span>  <br/> |<span data-ttu-id="3c98a-131">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3c98a-131">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98a-132">Optional</span><span class="sxs-lookup"><span data-stu-id="3c98a-132">optional</span></span>  <br/> ||<span data-ttu-id="3c98a-133">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3c98a-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98a-134">ID</span><span class="sxs-lookup"><span data-stu-id="3c98a-134">ID</span></span>  <br/> |<span data-ttu-id="3c98a-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3c98a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c98a-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3c98a-136">required</span></span>  <br/> ||<span data-ttu-id="3c98a-137">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3c98a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c98a-138">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="3c98a-138">Ignored</span></span>  <br/> |<span data-ttu-id="3c98a-139">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3c98a-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c98a-140">Optional</span><span class="sxs-lookup"><span data-stu-id="3c98a-140">optional</span></span>  <br/> ||<span data-ttu-id="3c98a-141">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3c98a-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c98a-142">NameU</span><span class="sxs-lookup"><span data-stu-id="3c98a-142">NameU</span></span>  <br/> |<span data-ttu-id="3c98a-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3c98a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="3c98a-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3c98a-144">required</span></span>  <br/> ||<span data-ttu-id="3c98a-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3c98a-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c98a-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="3c98a-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="3c98a-147">XSD: int</span><span class="sxs-lookup"><span data-stu-id="3c98a-147">xsd:int</span></span>  <br/> |<span data-ttu-id="3c98a-148">Optional</span><span class="sxs-lookup"><span data-stu-id="3c98a-148">optional</span></span>  <br/> ||<span data-ttu-id="3c98a-149">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3c98a-149">Values of the xsd:int type.</span></span>  <br/> |
   

