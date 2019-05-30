---
title: RuleSet-Element (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt einen Satz von Diagramm Validierungsregeln dar.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541638"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="71ca0-103">RuleSet-Element (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="71ca0-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="71ca0-104">Stellt einen Satz von Diagramm Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="71ca0-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71ca0-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="71ca0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71ca0-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="71ca0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="71ca0-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="71ca0-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="71ca0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="71ca0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="71ca0-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="71ca0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="71ca0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="71ca0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="71ca0-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="71ca0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="71ca0-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="71ca0-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71ca0-113">Definition</span><span class="sxs-lookup"><span data-stu-id="71ca0-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71ca0-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="71ca0-114">Elements and attributes</span></span>

<span data-ttu-id="71ca0-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="71ca0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="71ca0-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71ca0-116">Parent elements</span></span>

|<span data-ttu-id="71ca0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="71ca0-117">**Element**</span></span>|<span data-ttu-id="71ca0-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="71ca0-118">**Type**</span></span>|<span data-ttu-id="71ca0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71ca0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71ca0-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="71ca0-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71ca0-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="71ca0-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71ca0-122">Enthält ein **RuleSet** -Element für jeden Überprüfungsregel Satz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="71ca0-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="71ca0-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71ca0-123">Child elements</span></span>

|<span data-ttu-id="71ca0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="71ca0-124">**Element**</span></span>|<span data-ttu-id="71ca0-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="71ca0-125">**Type**</span></span>|<span data-ttu-id="71ca0-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71ca0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71ca0-127">Rule</span><span class="sxs-lookup"><span data-stu-id="71ca0-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71ca0-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="71ca0-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71ca0-129">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="71ca0-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="71ca0-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="71ca0-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71ca0-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="71ca0-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71ca0-132">Gibt Regel festgelegte Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="71ca0-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="71ca0-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="71ca0-133">Attributes</span></span>

|<span data-ttu-id="71ca0-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="71ca0-134">**Attribute**</span></span>|<span data-ttu-id="71ca0-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="71ca0-135">**Type**</span></span>|<span data-ttu-id="71ca0-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="71ca0-136">**Required**</span></span>|<span data-ttu-id="71ca0-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71ca0-137">**Description**</span></span>|<span data-ttu-id="71ca0-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="71ca0-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="71ca0-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71ca0-139">Description</span></span>  <br/> |<span data-ttu-id="71ca0-140">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71ca0-140">xsd:string</span></span>  <br/> |<span data-ttu-id="71ca0-141">Optional</span><span class="sxs-lookup"><span data-stu-id="71ca0-141">optional</span></span>  <br/> |<span data-ttu-id="71ca0-142">Gibt die Beschreibung an, die auf der Benutzeroberfläche des Validierungsregel Satzes angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="71ca0-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="71ca0-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="71ca0-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="71ca0-144">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="71ca0-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71ca0-145">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="71ca0-145">Enabled</span></span>  <br/> |<span data-ttu-id="71ca0-146">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="71ca0-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="71ca0-147">Optional</span><span class="sxs-lookup"><span data-stu-id="71ca0-147">optional</span></span>  <br/> |<span data-ttu-id="71ca0-148">Gibt an, ob die Regeln im angegebenen Überprüfungsregel Satz überprüft werden, wenn die Validierung für das aktuelle Dokument ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="71ca0-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="71ca0-149">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="71ca0-149">Default is True.</span></span>  <br/> |<span data-ttu-id="71ca0-150">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="71ca0-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="71ca0-151">ID</span><span class="sxs-lookup"><span data-stu-id="71ca0-151">ID</span></span>  <br/> |<span data-ttu-id="71ca0-152">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="71ca0-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="71ca0-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ca0-153">required</span></span>  <br/> |<span data-ttu-id="71ca0-154">Gibt den eindeutigen Bezeichner des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="71ca0-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="71ca0-155">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="71ca0-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="71ca0-156">Name</span><span class="sxs-lookup"><span data-stu-id="71ca0-156">Name</span></span>  <br/> |<span data-ttu-id="71ca0-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71ca0-157">xsd:string</span></span>  <br/> |<span data-ttu-id="71ca0-158">Optional</span><span class="sxs-lookup"><span data-stu-id="71ca0-158">optional</span></span>  <br/> |<span data-ttu-id="71ca0-159">Gibt den lokalen Namen des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="71ca0-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="71ca0-160">Standardwert NameU-Attribut.</span><span class="sxs-lookup"><span data-stu-id="71ca0-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="71ca0-161">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="71ca0-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71ca0-162">NameU</span><span class="sxs-lookup"><span data-stu-id="71ca0-162">NameU</span></span>  <br/> |<span data-ttu-id="71ca0-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="71ca0-163">xsd:string</span></span>  <br/> |<span data-ttu-id="71ca0-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ca0-164">required</span></span>  <br/> |<span data-ttu-id="71ca0-165">Gibt den universellen Namen des Überprüfungsregel Satzes an.</span><span class="sxs-lookup"><span data-stu-id="71ca0-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="71ca0-166">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="71ca0-166">Values of the xsd:string type.</span></span>  <br/> |
   

