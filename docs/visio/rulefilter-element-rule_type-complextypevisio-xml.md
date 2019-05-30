---
title: RuleFilter-Element (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Gibt den logischen Ausdruck an, der bestimmt, ob die Validierungsregel auf ein Zielobjekt angewendet werden soll.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541680"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="059f3-103">RuleFilter-Element (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="059f3-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="059f3-104">Gibt den logischen Ausdruck an, der bestimmt, ob die Validierungsregel auf ein Zielobjekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="059f3-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="059f3-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="059f3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="059f3-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="059f3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="059f3-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="059f3-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="059f3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="059f3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="059f3-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="059f3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="059f3-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="059f3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="059f3-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="059f3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="059f3-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="059f3-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="059f3-113">Definition</span><span class="sxs-lookup"><span data-stu-id="059f3-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="059f3-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="059f3-114">Elements and attributes</span></span>

<span data-ttu-id="059f3-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="059f3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="059f3-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="059f3-116">Parent elements</span></span>

|<span data-ttu-id="059f3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="059f3-117">**Element**</span></span>|<span data-ttu-id="059f3-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="059f3-118">**Type**</span></span>|<span data-ttu-id="059f3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="059f3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="059f3-120">Rule</span><span class="sxs-lookup"><span data-stu-id="059f3-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="059f3-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="059f3-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="059f3-122">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="059f3-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="059f3-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="059f3-123">Child elements</span></span>

<span data-ttu-id="059f3-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="059f3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="059f3-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="059f3-125">Attributes</span></span>

|<span data-ttu-id="059f3-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="059f3-126">**Attribute**</span></span>|<span data-ttu-id="059f3-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="059f3-127">**Type**</span></span>|<span data-ttu-id="059f3-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="059f3-128">**Required**</span></span>|<span data-ttu-id="059f3-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="059f3-129">**Description**</span></span>|<span data-ttu-id="059f3-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="059f3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="059f3-131">Formel</span><span class="sxs-lookup"><span data-stu-id="059f3-131">Formula</span></span>  <br/> |<span data-ttu-id="059f3-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="059f3-132">xsd:string</span></span>  <br/> |<span data-ttu-id="059f3-133">Optional</span><span class="sxs-lookup"><span data-stu-id="059f3-133">optional</span></span>  <br/> |<span data-ttu-id="059f3-134">Stellt die Formel des Elements dar.</span><span class="sxs-lookup"><span data-stu-id="059f3-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="059f3-135">Werte der XSD: String.</span><span class="sxs-lookup"><span data-stu-id="059f3-135">Values of the xsd:string.</span></span>  <br/> |
   

