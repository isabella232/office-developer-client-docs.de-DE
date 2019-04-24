---
title: RuleSet-Element (RuleSets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt einen Satz von Diagramm Validierungsregeln dar.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318914"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="79eb2-103">RuleSet-Element (RuleSets_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="79eb2-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="79eb2-104">Stellt einen Satz von Diagramm Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="79eb2-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79eb2-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="79eb2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79eb2-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="79eb2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="79eb2-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="79eb2-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="79eb2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="79eb2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="79eb2-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="79eb2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="79eb2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="79eb2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="79eb2-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="79eb2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="79eb2-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="79eb2-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79eb2-113">Definition</span><span class="sxs-lookup"><span data-stu-id="79eb2-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="79eb2-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="79eb2-114">Elements and attributes</span></span>

<span data-ttu-id="79eb2-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="79eb2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="79eb2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79eb2-116">Parent elements</span></span>

|<span data-ttu-id="79eb2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="79eb2-117">**Element**</span></span>|<span data-ttu-id="79eb2-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="79eb2-118">**Type**</span></span>|<span data-ttu-id="79eb2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79eb2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79eb2-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="79eb2-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="79eb2-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="79eb2-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="79eb2-122">Enthält ein **RuleSet** -Element für jeden Überprüfungsregel Satz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="79eb2-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="79eb2-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79eb2-123">Child elements</span></span>

|<span data-ttu-id="79eb2-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="79eb2-124">**Element**</span></span>|<span data-ttu-id="79eb2-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="79eb2-125">**Type**</span></span>|<span data-ttu-id="79eb2-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79eb2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79eb2-127">Rule</span><span class="sxs-lookup"><span data-stu-id="79eb2-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="79eb2-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="79eb2-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="79eb2-129">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="79eb2-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="79eb2-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="79eb2-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="79eb2-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="79eb2-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="79eb2-132">Gibt Regel Satz Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="79eb2-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="79eb2-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="79eb2-133">Attributes</span></span>

|<span data-ttu-id="79eb2-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="79eb2-134">**Attribute**</span></span>|<span data-ttu-id="79eb2-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="79eb2-135">**Type**</span></span>|<span data-ttu-id="79eb2-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="79eb2-136">**Required**</span></span>|<span data-ttu-id="79eb2-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79eb2-137">**Description**</span></span>|<span data-ttu-id="79eb2-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="79eb2-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="79eb2-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79eb2-139">Description</span></span>  <br/> |<span data-ttu-id="79eb2-140">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79eb2-140">xsd:string</span></span>  <br/> |<span data-ttu-id="79eb2-141">Optional</span><span class="sxs-lookup"><span data-stu-id="79eb2-141">optional</span></span>  <br/> |<span data-ttu-id="79eb2-142">Gibt die Beschreibung an, die auf der Benutzeroberfläche für den Überprüfungsregel Satz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="79eb2-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="79eb2-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="79eb2-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="79eb2-144">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="79eb2-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79eb2-145">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="79eb2-145">Enabled</span></span>  <br/> |<span data-ttu-id="79eb2-146">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="79eb2-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="79eb2-147">Optional</span><span class="sxs-lookup"><span data-stu-id="79eb2-147">optional</span></span>  <br/> |<span data-ttu-id="79eb2-148">Gibt an, ob die Regeln im angegebenen Validierungsregel Satz beim Auslösen der Validierung für das aktuelle Dokument überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="79eb2-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="79eb2-149">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="79eb2-149">Default is True.</span></span>  <br/> |<span data-ttu-id="79eb2-150">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="79eb2-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="79eb2-151">ID</span><span class="sxs-lookup"><span data-stu-id="79eb2-151">ID</span></span>  <br/> |<span data-ttu-id="79eb2-152">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="79eb2-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="79eb2-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="79eb2-153">required</span></span>  <br/> |<span data-ttu-id="79eb2-154">Gibt den eindeutigen Bezeichner des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="79eb2-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="79eb2-155">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="79eb2-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="79eb2-156">Name</span><span class="sxs-lookup"><span data-stu-id="79eb2-156">Name</span></span>  <br/> |<span data-ttu-id="79eb2-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79eb2-157">xsd:string</span></span>  <br/> |<span data-ttu-id="79eb2-158">Optional</span><span class="sxs-lookup"><span data-stu-id="79eb2-158">optional</span></span>  <br/> |<span data-ttu-id="79eb2-159">Gibt den lokalen Namen des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="79eb2-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="79eb2-160">Defaults to NameU-Attributwert.</span><span class="sxs-lookup"><span data-stu-id="79eb2-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="79eb2-161">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="79eb2-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79eb2-162">NameU</span><span class="sxs-lookup"><span data-stu-id="79eb2-162">NameU</span></span>  <br/> |<span data-ttu-id="79eb2-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79eb2-163">xsd:string</span></span>  <br/> |<span data-ttu-id="79eb2-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="79eb2-164">required</span></span>  <br/> |<span data-ttu-id="79eb2-165">Gibt den universellen Namen des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="79eb2-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="79eb2-166">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="79eb2-166">Values of the xsd:string type.</span></span>  <br/> |
   

