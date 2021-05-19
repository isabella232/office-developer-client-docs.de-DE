---
title: Rule-Element (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541708"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="40d4b-103">Rule-Element (RuleSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="40d4b-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="40d4b-104">Repräsentiert eine einzelne Überprüfungsregel in einem Regelsatz für die Diagrammüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="40d4b-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40d4b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="40d4b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40d4b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="40d4b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="40d4b-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="40d4b-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="40d4b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="40d4b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="40d4b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="40d4b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="40d4b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="40d4b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="40d4b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="40d4b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="40d4b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="40d4b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40d4b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="40d4b-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="40d4b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="40d4b-114">Elements and attributes</span></span>

<span data-ttu-id="40d4b-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="40d4b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="40d4b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40d4b-116">Parent elements</span></span>

|<span data-ttu-id="40d4b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="40d4b-117">**Element**</span></span>|<span data-ttu-id="40d4b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="40d4b-118">**Type**</span></span>|<span data-ttu-id="40d4b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40d4b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40d4b-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="40d4b-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40d4b-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="40d4b-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40d4b-122">Stellt einen Satz von Diagrammüberprüfungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="40d4b-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40d4b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40d4b-123">Child elements</span></span>

|<span data-ttu-id="40d4b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="40d4b-124">**Element**</span></span>|<span data-ttu-id="40d4b-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="40d4b-125">**Type**</span></span>|<span data-ttu-id="40d4b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40d4b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40d4b-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="40d4b-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40d4b-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="40d4b-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40d4b-129">Gibt den logischen Ausdruck an, der bestimmt, ob die Gültigkeitsprüfungsregel auf ein Zielobjekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="40d4b-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="40d4b-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="40d4b-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40d4b-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="40d4b-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40d4b-132">Gibt den logischen Ausdruck an, der bestimmt, ob das Zielobjekt der Gültigkeitsprüfungsregel entspricht.</span><span class="sxs-lookup"><span data-stu-id="40d4b-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="40d4b-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="40d4b-133">Attributes</span></span>

|<span data-ttu-id="40d4b-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="40d4b-134">**Attribute**</span></span>|<span data-ttu-id="40d4b-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="40d4b-135">**Type**</span></span>|<span data-ttu-id="40d4b-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="40d4b-136">**Required**</span></span>|<span data-ttu-id="40d4b-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40d4b-137">**Description**</span></span>|<span data-ttu-id="40d4b-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="40d4b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40d4b-139">Kategorie</span><span class="sxs-lookup"><span data-stu-id="40d4b-139">Category</span></span>  <br/> |<span data-ttu-id="40d4b-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="40d4b-140">xsd:string</span></span>  <br/> |<span data-ttu-id="40d4b-141">Optional</span><span class="sxs-lookup"><span data-stu-id="40d4b-141">optional</span></span>  <br/> |<span data-ttu-id="40d4b-142">Gibt den Text an, der in der **Spalte Kategorie** des Fensters Probleme angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="40d4b-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="40d4b-143">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="40d4b-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="40d4b-144">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="40d4b-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="40d4b-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40d4b-145">Description</span></span>  <br/> |<span data-ttu-id="40d4b-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="40d4b-146">xsd:string</span></span>  <br/> |<span data-ttu-id="40d4b-147">Optional</span><span class="sxs-lookup"><span data-stu-id="40d4b-147">optional</span></span>  <br/> |<span data-ttu-id="40d4b-148">Gibt die Beschreibung der Überprüfungsregel an, die auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="40d4b-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="40d4b-149">Der Standardwert ist "Unknown".</span><span class="sxs-lookup"><span data-stu-id="40d4b-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="40d4b-150">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="40d4b-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="40d4b-151">ID</span><span class="sxs-lookup"><span data-stu-id="40d4b-151">ID</span></span>  <br/> |<span data-ttu-id="40d4b-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="40d4b-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40d4b-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="40d4b-153">required</span></span>  <br/> |<span data-ttu-id="40d4b-154">Gibt den eindeutigen Bezeichner für die Gültigkeitsprüfungsregel an.</span><span class="sxs-lookup"><span data-stu-id="40d4b-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="40d4b-155">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="40d4b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40d4b-156">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="40d4b-156">Ignored</span></span>  <br/> |<span data-ttu-id="40d4b-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="40d4b-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="40d4b-158">Optional</span><span class="sxs-lookup"><span data-stu-id="40d4b-158">optional</span></span>  <br/> |<span data-ttu-id="40d4b-159">Gibt an, ob die Gültigkeitsprüfungsregel derzeit ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="40d4b-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="40d4b-160">Der Standardwert ist False.</span><span class="sxs-lookup"><span data-stu-id="40d4b-160">Default is False.</span></span>  <br/> |<span data-ttu-id="40d4b-161">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="40d4b-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="40d4b-162">NameU</span><span class="sxs-lookup"><span data-stu-id="40d4b-162">NameU</span></span>  <br/> |<span data-ttu-id="40d4b-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="40d4b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="40d4b-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="40d4b-164">required</span></span>  <br/> |<span data-ttu-id="40d4b-165">Gibt den universellen Namen der Gültigkeitsprüfungsregel an.</span><span class="sxs-lookup"><span data-stu-id="40d4b-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="40d4b-166">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="40d4b-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="40d4b-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="40d4b-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="40d4b-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="40d4b-168">xsd:int</span></span>  <br/> |<span data-ttu-id="40d4b-169">Optional</span><span class="sxs-lookup"><span data-stu-id="40d4b-169">optional</span></span>  <br/> |<span data-ttu-id="40d4b-170">Gibt den Objekttyp an, auf den die Überprüfungsregel angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="40d4b-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="40d4b-171">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="40d4b-171">Values of the xsd:int type.</span></span>  <br/> |
   

