---
title: RuleSet-Element (RuleSets_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt eine Reihe von Diagramm-Validierungsregeln dar.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797954"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="1cb07-103">RuleSet-Element (RuleSets_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="1cb07-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1cb07-104">Stellt eine Reihe von Diagramm-Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="1cb07-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1cb07-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1cb07-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cb07-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1cb07-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1cb07-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="1cb07-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1cb07-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1cb07-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1cb07-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1cb07-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1cb07-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1cb07-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1cb07-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="1cb07-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1cb07-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="1cb07-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cb07-113">Definition</span><span class="sxs-lookup"><span data-stu-id="1cb07-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1cb07-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1cb07-114">Elements and attributes</span></span>

<span data-ttu-id="1cb07-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1cb07-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1cb07-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1cb07-116">Parent elements</span></span>

|<span data-ttu-id="1cb07-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1cb07-117">**Element**</span></span>|<span data-ttu-id="1cb07-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1cb07-118">**Type**</span></span>|<span data-ttu-id="1cb07-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1cb07-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1cb07-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="1cb07-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1cb07-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="1cb07-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1cb07-122">Enthält ein **RuleSet** -Element für jeden überprüfungsregelsatz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="1cb07-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1cb07-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1cb07-123">Child elements</span></span>

|<span data-ttu-id="1cb07-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1cb07-124">**Element**</span></span>|<span data-ttu-id="1cb07-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1cb07-125">**Type**</span></span>|<span data-ttu-id="1cb07-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1cb07-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1cb07-127">Rule</span><span class="sxs-lookup"><span data-stu-id="1cb07-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1cb07-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="1cb07-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1cb07-129">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="1cb07-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="1cb07-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="1cb07-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1cb07-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="1cb07-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1cb07-132">Gibt Regelsatz-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cb07-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1cb07-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="1cb07-133">Attributes</span></span>

|<span data-ttu-id="1cb07-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1cb07-134">**Attribute**</span></span>|<span data-ttu-id="1cb07-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1cb07-135">**Type**</span></span>|<span data-ttu-id="1cb07-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1cb07-136">**Required**</span></span>|<span data-ttu-id="1cb07-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1cb07-137">**Description**</span></span>|<span data-ttu-id="1cb07-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1cb07-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cb07-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cb07-139">Description</span></span>  <br/> |<span data-ttu-id="1cb07-140">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1cb07-140">xsd:string</span></span>  <br/> |<span data-ttu-id="1cb07-141">Optional</span><span class="sxs-lookup"><span data-stu-id="1cb07-141">optional</span></span>  <br/> |<span data-ttu-id="1cb07-142">Gibt die Beschreibung, die in der Benutzeroberfläche für die Überprüfungsregel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1cb07-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="1cb07-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1cb07-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="1cb07-144">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1cb07-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cb07-145">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="1cb07-145">Enabled</span></span>  <br/> |<span data-ttu-id="1cb07-146">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="1cb07-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1cb07-147">Optional</span><span class="sxs-lookup"><span data-stu-id="1cb07-147">optional</span></span>  <br/> |<span data-ttu-id="1cb07-148">Gibt an, ob die Regeln in der angegebenen Regelsatz überprüft werden, wenn Validierung für das aktuelle Dokument ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="1cb07-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="1cb07-149">Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="1cb07-149">Default is True.</span></span>  <br/> |<span data-ttu-id="1cb07-150">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1cb07-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1cb07-151">ID</span><span class="sxs-lookup"><span data-stu-id="1cb07-151">ID</span></span>  <br/> |<span data-ttu-id="1cb07-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cb07-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cb07-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1cb07-153">required</span></span>  <br/> |<span data-ttu-id="1cb07-154">Gibt den eindeutigen Bezeichner der der Überprüfungsregel.</span><span class="sxs-lookup"><span data-stu-id="1cb07-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="1cb07-155">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cb07-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cb07-156">Name</span><span class="sxs-lookup"><span data-stu-id="1cb07-156">Name</span></span>  <br/> |<span data-ttu-id="1cb07-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1cb07-157">xsd:string</span></span>  <br/> |<span data-ttu-id="1cb07-158">Optional</span><span class="sxs-lookup"><span data-stu-id="1cb07-158">optional</span></span>  <br/> |<span data-ttu-id="1cb07-159">Gibt den lokalen Namen der der Überprüfungsregel an.</span><span class="sxs-lookup"><span data-stu-id="1cb07-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="1cb07-160">Der Standardwert ist NameU-Attributwert.</span><span class="sxs-lookup"><span data-stu-id="1cb07-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="1cb07-161">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1cb07-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cb07-162">NameU</span><span class="sxs-lookup"><span data-stu-id="1cb07-162">NameU</span></span>  <br/> |<span data-ttu-id="1cb07-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1cb07-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1cb07-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1cb07-164">required</span></span>  <br/> |<span data-ttu-id="1cb07-165">Gibt den universellen Namen eines der Überprüfungsregel an.</span><span class="sxs-lookup"><span data-stu-id="1cb07-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="1cb07-166">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1cb07-166">Values of the xsd:string type.</span></span>  <br/> |
   

