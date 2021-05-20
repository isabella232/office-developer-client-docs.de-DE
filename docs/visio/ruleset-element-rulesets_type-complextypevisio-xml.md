---
title: RuleSet-Element (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Stellt einen Satz von Diagrammüberprüfungsregeln dar.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541638"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="9d54a-103">RuleSet-Element (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9d54a-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9d54a-104">Stellt einen Satz von Diagrammüberprüfungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="9d54a-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d54a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d54a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d54a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9d54a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9d54a-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9d54a-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9d54a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d54a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9d54a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9d54a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9d54a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9d54a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9d54a-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="9d54a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9d54a-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="9d54a-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d54a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9d54a-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d54a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9d54a-114">Elements and attributes</span></span>

<span data-ttu-id="9d54a-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9d54a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d54a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d54a-116">Parent elements</span></span>

|<span data-ttu-id="9d54a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d54a-117">**Element**</span></span>|<span data-ttu-id="9d54a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9d54a-118">**Type**</span></span>|<span data-ttu-id="9d54a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d54a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d54a-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="9d54a-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d54a-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="9d54a-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d54a-122">Enthält ein **RuleSet-Element** für jeden Überprüfungsregelsatz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="9d54a-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d54a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d54a-123">Child elements</span></span>

|<span data-ttu-id="9d54a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d54a-124">**Element**</span></span>|<span data-ttu-id="9d54a-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9d54a-125">**Type**</span></span>|<span data-ttu-id="9d54a-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d54a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d54a-127">Rule</span><span class="sxs-lookup"><span data-stu-id="9d54a-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d54a-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9d54a-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d54a-129">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="9d54a-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="9d54a-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="9d54a-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d54a-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="9d54a-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d54a-132">Gibt Eigenschaften für Regelsatz an.</span><span class="sxs-lookup"><span data-stu-id="9d54a-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9d54a-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d54a-133">Attributes</span></span>

|<span data-ttu-id="9d54a-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9d54a-134">**Attribute**</span></span>|<span data-ttu-id="9d54a-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9d54a-135">**Type**</span></span>|<span data-ttu-id="9d54a-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9d54a-136">**Required**</span></span>|<span data-ttu-id="9d54a-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d54a-137">**Description**</span></span>|<span data-ttu-id="9d54a-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9d54a-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d54a-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d54a-139">Description</span></span>  <br/> |<span data-ttu-id="9d54a-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d54a-140">xsd:string</span></span>  <br/> |<span data-ttu-id="9d54a-141">Optional</span><span class="sxs-lookup"><span data-stu-id="9d54a-141">optional</span></span>  <br/> |<span data-ttu-id="9d54a-142">Gibt die Beschreibung an, die auf der Benutzeroberfläche für den Überprüfungsregelsatz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9d54a-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="9d54a-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9d54a-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="9d54a-144">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="9d54a-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9d54a-145">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="9d54a-145">Enabled</span></span>  <br/> |<span data-ttu-id="9d54a-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9d54a-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9d54a-147">Optional</span><span class="sxs-lookup"><span data-stu-id="9d54a-147">optional</span></span>  <br/> |<span data-ttu-id="9d54a-148">Gibt an, ob die Regeln im angegebenen Überprüfungsregelsatz überprüft werden, wenn die Überprüfung für das aktuelle Dokument ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="9d54a-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="9d54a-149">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="9d54a-149">Default is True.</span></span>  <br/> |<span data-ttu-id="9d54a-150">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9d54a-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9d54a-151">ID</span><span class="sxs-lookup"><span data-stu-id="9d54a-151">ID</span></span>  <br/> |<span data-ttu-id="9d54a-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9d54a-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9d54a-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9d54a-153">required</span></span>  <br/> |<span data-ttu-id="9d54a-154">Gibt den eindeutigen Bezeichner des Überprüfungsregelsatzs an.</span><span class="sxs-lookup"><span data-stu-id="9d54a-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="9d54a-155">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9d54a-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9d54a-156">Name</span><span class="sxs-lookup"><span data-stu-id="9d54a-156">Name</span></span>  <br/> |<span data-ttu-id="9d54a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d54a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="9d54a-158">Optional</span><span class="sxs-lookup"><span data-stu-id="9d54a-158">optional</span></span>  <br/> |<span data-ttu-id="9d54a-159">Gibt den lokalen Namen des Überprüfungsregelsatzs an.</span><span class="sxs-lookup"><span data-stu-id="9d54a-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="9d54a-160">Standardmäßig wird der NameU-Attributwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d54a-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="9d54a-161">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="9d54a-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9d54a-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9d54a-162">NameU</span></span>  <br/> |<span data-ttu-id="9d54a-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9d54a-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9d54a-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9d54a-164">required</span></span>  <br/> |<span data-ttu-id="9d54a-165">Gibt den universellen Namen des Überprüfungsregelsatzs an.</span><span class="sxs-lookup"><span data-stu-id="9d54a-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="9d54a-166">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="9d54a-166">Values of the xsd:string type.</span></span>  <br/> |
   

