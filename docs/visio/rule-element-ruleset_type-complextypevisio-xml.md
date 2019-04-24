---
title: Rule-Element (RuleSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358800"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="65f08-103">Rule-Element (RuleSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="65f08-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="65f08-104">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="65f08-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65f08-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="65f08-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65f08-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="65f08-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65f08-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="65f08-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65f08-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65f08-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65f08-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="65f08-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65f08-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="65f08-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65f08-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="65f08-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65f08-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="65f08-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65f08-113">Definition</span><span class="sxs-lookup"><span data-stu-id="65f08-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65f08-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="65f08-114">Elements and attributes</span></span>

<span data-ttu-id="65f08-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="65f08-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65f08-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65f08-116">Parent elements</span></span>

|<span data-ttu-id="65f08-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="65f08-117">**Element**</span></span>|<span data-ttu-id="65f08-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="65f08-118">**Type**</span></span>|<span data-ttu-id="65f08-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65f08-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65f08-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="65f08-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65f08-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="65f08-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65f08-122">Stellt einen Satz von Diagramm Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="65f08-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65f08-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65f08-123">Child elements</span></span>

|<span data-ttu-id="65f08-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="65f08-124">**Element**</span></span>|<span data-ttu-id="65f08-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="65f08-125">**Type**</span></span>|<span data-ttu-id="65f08-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65f08-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65f08-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="65f08-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65f08-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="65f08-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65f08-129">Gibt den logischen Ausdruck an, der bestimmt, ob die Validierungsregel auf ein Zielobjekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="65f08-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="65f08-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="65f08-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65f08-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="65f08-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65f08-132">Gibt den logischen Ausdruck an, der bestimmt, ob das Zielobjekt der Validierungsregel entspricht.</span><span class="sxs-lookup"><span data-stu-id="65f08-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="65f08-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="65f08-133">Attributes</span></span>

|<span data-ttu-id="65f08-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="65f08-134">**Attribute**</span></span>|<span data-ttu-id="65f08-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="65f08-135">**Type**</span></span>|<span data-ttu-id="65f08-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="65f08-136">**Required**</span></span>|<span data-ttu-id="65f08-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65f08-137">**Description**</span></span>|<span data-ttu-id="65f08-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="65f08-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65f08-139">Kategorie</span><span class="sxs-lookup"><span data-stu-id="65f08-139">Category</span></span>  <br/> |<span data-ttu-id="65f08-140">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f08-140">xsd:string</span></span>  <br/> |<span data-ttu-id="65f08-141">Optional</span><span class="sxs-lookup"><span data-stu-id="65f08-141">optional</span></span>  <br/> |<span data-ttu-id="65f08-142">Gibt den Text an, der in der Spalte **Kategorie** des Fensters Probleme angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="65f08-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="65f08-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="65f08-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="65f08-144">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65f08-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65f08-145">Description</span></span>  <br/> |<span data-ttu-id="65f08-146">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f08-146">xsd:string</span></span>  <br/> |<span data-ttu-id="65f08-147">Optional</span><span class="sxs-lookup"><span data-stu-id="65f08-147">optional</span></span>  <br/> |<span data-ttu-id="65f08-148">Gibt die Beschreibung der Validierungsregel an, die auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="65f08-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="65f08-149">Der Standardwert ist "unknown".</span><span class="sxs-lookup"><span data-stu-id="65f08-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="65f08-150">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65f08-151">ID</span><span class="sxs-lookup"><span data-stu-id="65f08-151">ID</span></span>  <br/> |<span data-ttu-id="65f08-152">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65f08-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65f08-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="65f08-153">required</span></span>  <br/> |<span data-ttu-id="65f08-154">Gibt den eindeutigen Bezeichner für die Validierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="65f08-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="65f08-155">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65f08-156">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="65f08-156">Ignored</span></span>  <br/> |<span data-ttu-id="65f08-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="65f08-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65f08-158">Optional</span><span class="sxs-lookup"><span data-stu-id="65f08-158">optional</span></span>  <br/> |<span data-ttu-id="65f08-159">Gibt an, ob die Validierungsregel derzeit ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="65f08-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="65f08-160">Der Standardwert ist False.</span><span class="sxs-lookup"><span data-stu-id="65f08-160">Default is False.</span></span>  <br/> |<span data-ttu-id="65f08-161">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="65f08-162">NameU</span><span class="sxs-lookup"><span data-stu-id="65f08-162">NameU</span></span>  <br/> |<span data-ttu-id="65f08-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="65f08-163">xsd:string</span></span>  <br/> |<span data-ttu-id="65f08-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="65f08-164">required</span></span>  <br/> |<span data-ttu-id="65f08-165">Gibt den universellen Namen der Validierungsregel an.</span><span class="sxs-lookup"><span data-stu-id="65f08-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="65f08-166">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65f08-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="65f08-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="65f08-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="65f08-168">xsd:int</span></span>  <br/> |<span data-ttu-id="65f08-169">Optional</span><span class="sxs-lookup"><span data-stu-id="65f08-169">optional</span></span>  <br/> |<span data-ttu-id="65f08-170">Gibt den Objekttyp an, auf den die Validierungsregel angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="65f08-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="65f08-171">Werte des XSD: int-Typs.</span><span class="sxs-lookup"><span data-stu-id="65f08-171">Values of the xsd:int type.</span></span>  <br/> |
   

