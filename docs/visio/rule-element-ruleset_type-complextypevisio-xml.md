---
title: Rule-Element (RuleSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797934"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="4b483-103">Rule-Element (RuleSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4b483-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4b483-104">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="4b483-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b483-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4b483-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b483-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4b483-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4b483-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="4b483-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4b483-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4b483-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4b483-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4b483-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4b483-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4b483-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4b483-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="4b483-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4b483-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="4b483-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b483-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4b483-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4b483-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4b483-114">Elements and attributes</span></span>

<span data-ttu-id="4b483-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4b483-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4b483-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b483-116">Parent elements</span></span>

|<span data-ttu-id="4b483-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b483-117">**Element**</span></span>|<span data-ttu-id="4b483-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4b483-118">**Type**</span></span>|<span data-ttu-id="4b483-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b483-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b483-120">Regelsatz</span><span class="sxs-lookup"><span data-stu-id="4b483-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b483-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="4b483-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b483-122">Stellt eine Reihe von Diagramm-Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="4b483-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b483-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4b483-123">Child elements</span></span>

|<span data-ttu-id="4b483-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b483-124">**Element**</span></span>|<span data-ttu-id="4b483-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4b483-125">**Type**</span></span>|<span data-ttu-id="4b483-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b483-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b483-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="4b483-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b483-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="4b483-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b483-129">Gibt den logischen Ausdruck, der bestimmt, ob der Überprüfungsregel auf ein Zielobjekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b483-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="4b483-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="4b483-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b483-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="4b483-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b483-132">Gibt den logischen Ausdruck, der bestimmt, ob das Zielobjekt der Überprüfungsregel erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4b483-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4b483-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="4b483-133">Attributes</span></span>

|<span data-ttu-id="4b483-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4b483-134">**Attribute**</span></span>|<span data-ttu-id="4b483-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4b483-135">**Type**</span></span>|<span data-ttu-id="4b483-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4b483-136">**Required**</span></span>|<span data-ttu-id="4b483-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b483-137">**Description**</span></span>|<span data-ttu-id="4b483-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4b483-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b483-139">Kategorie</span><span class="sxs-lookup"><span data-stu-id="4b483-139">Category</span></span>  <br/> |<span data-ttu-id="4b483-140">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4b483-140">xsd:string</span></span>  <br/> |<span data-ttu-id="4b483-141">Optional</span><span class="sxs-lookup"><span data-stu-id="4b483-141">optional</span></span>  <br/> |<span data-ttu-id="4b483-142">Gibt den Text in der **Kategorie** -Spalte der Problemfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b483-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="4b483-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b483-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="4b483-144">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4b483-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b483-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b483-145">Description</span></span>  <br/> |<span data-ttu-id="4b483-146">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4b483-146">xsd:string</span></span>  <br/> |<span data-ttu-id="4b483-147">Optional</span><span class="sxs-lookup"><span data-stu-id="4b483-147">optional</span></span>  <br/> |<span data-ttu-id="4b483-148">Gibt die Beschreibung der Überprüfungsregel, die in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b483-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="4b483-149">Der Standardwert lautet "Unknown".</span><span class="sxs-lookup"><span data-stu-id="4b483-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="4b483-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4b483-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b483-151">ID</span><span class="sxs-lookup"><span data-stu-id="4b483-151">ID</span></span>  <br/> |<span data-ttu-id="4b483-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b483-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b483-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4b483-153">required</span></span>  <br/> |<span data-ttu-id="4b483-154">Gibt den eindeutigen Bezeichner für die Überprüfungsregel.</span><span class="sxs-lookup"><span data-stu-id="4b483-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="4b483-155">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b483-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b483-156">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="4b483-156">Ignored</span></span>  <br/> |<span data-ttu-id="4b483-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4b483-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4b483-158">Optional</span><span class="sxs-lookup"><span data-stu-id="4b483-158">optional</span></span>  <br/> |<span data-ttu-id="4b483-159">Gibt an, ob der Überprüfungsregel derzeit ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="4b483-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="4b483-160">Standard ist False.</span><span class="sxs-lookup"><span data-stu-id="4b483-160">Default is False.</span></span>  <br/> |<span data-ttu-id="4b483-161">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4b483-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4b483-162">NameU</span><span class="sxs-lookup"><span data-stu-id="4b483-162">NameU</span></span>  <br/> |<span data-ttu-id="4b483-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4b483-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4b483-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4b483-164">required</span></span>  <br/> |<span data-ttu-id="4b483-165">Gibt den universellen Namen der Überprüfungsregel.</span><span class="sxs-lookup"><span data-stu-id="4b483-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="4b483-166">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4b483-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b483-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="4b483-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="4b483-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="4b483-168">xsd:int</span></span>  <br/> |<span data-ttu-id="4b483-169">Optional</span><span class="sxs-lookup"><span data-stu-id="4b483-169">optional</span></span>  <br/> |<span data-ttu-id="4b483-170">Gibt den Typ des Objekts an die der Überprüfungsregel angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b483-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="4b483-171">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="4b483-171">Values of the xsd:int type.</span></span>  <br/> |
   

