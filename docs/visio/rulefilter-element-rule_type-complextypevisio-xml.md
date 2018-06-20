---
title: RuleFilter-Element (Rule_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797929"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="171eb-103">RuleFilter-Element (Rule_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="171eb-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="171eb-104">Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="171eb-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="171eb-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="171eb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="171eb-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="171eb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="171eb-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="171eb-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="171eb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="171eb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="171eb-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="171eb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="171eb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="171eb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="171eb-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="171eb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="171eb-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="171eb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="171eb-113">Definition</span><span class="sxs-lookup"><span data-stu-id="171eb-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="171eb-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="171eb-114">Elements and attributes</span></span>

<span data-ttu-id="171eb-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="171eb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="171eb-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="171eb-116">Parent elements</span></span>

|<span data-ttu-id="171eb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="171eb-117">**Element**</span></span>|<span data-ttu-id="171eb-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="171eb-118">**Type**</span></span>|<span data-ttu-id="171eb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="171eb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="171eb-120">Rule</span><span class="sxs-lookup"><span data-stu-id="171eb-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="171eb-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="171eb-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="171eb-122">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="171eb-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="171eb-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="171eb-123">Child elements</span></span>

<span data-ttu-id="171eb-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="171eb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="171eb-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="171eb-125">Attributes</span></span>

|<span data-ttu-id="171eb-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="171eb-126">**Attribute**</span></span>|<span data-ttu-id="171eb-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="171eb-127">**Type**</span></span>|<span data-ttu-id="171eb-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="171eb-128">**Required**</span></span>|<span data-ttu-id="171eb-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="171eb-129">**Description**</span></span>|<span data-ttu-id="171eb-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="171eb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="171eb-131">Formel</span><span class="sxs-lookup"><span data-stu-id="171eb-131">Formula</span></span>  <br/> |<span data-ttu-id="171eb-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="171eb-132">xsd:string</span></span>  <br/> |<span data-ttu-id="171eb-133">Optional</span><span class="sxs-lookup"><span data-stu-id="171eb-133">optional</span></span>  <br/> |<span data-ttu-id="171eb-134">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="171eb-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="171eb-135">Die Werte für die XSD: String.</span><span class="sxs-lookup"><span data-stu-id="171eb-135">Values of the xsd:string.</span></span>  <br/> |
   

