---
title: Problem-Element (Issues_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Überprüfungsproblem im Dokument.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389841"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="9ce20-103">Problem-Element (Issues_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="9ce20-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9ce20-104">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="9ce20-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ce20-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9ce20-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ce20-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9ce20-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9ce20-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="9ce20-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9ce20-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ce20-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9ce20-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9ce20-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9ce20-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9ce20-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9ce20-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="9ce20-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9ce20-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="9ce20-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ce20-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9ce20-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ce20-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9ce20-114">Elements and attributes</span></span>

<span data-ttu-id="9ce20-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="9ce20-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9ce20-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ce20-116">Parent elements</span></span>

|<span data-ttu-id="9ce20-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ce20-117">**Element**</span></span>|<span data-ttu-id="9ce20-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ce20-118">**Type**</span></span>|<span data-ttu-id="9ce20-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ce20-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ce20-120">Probleme</span><span class="sxs-lookup"><span data-stu-id="9ce20-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ce20-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="9ce20-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ce20-122">Enthält alle **Problem** Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="9ce20-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ce20-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ce20-123">Child elements</span></span>

|<span data-ttu-id="9ce20-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ce20-124">**Element**</span></span>|<span data-ttu-id="9ce20-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ce20-125">**Type**</span></span>|<span data-ttu-id="9ce20-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ce20-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ce20-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="9ce20-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ce20-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="9ce20-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ce20-129">Je nach das Ziel des übergeordneten gibt Überprüfungsproblem, entweder die Seite oder die Seite und die Form, der übergeordnete Überprüfungsproblem zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9ce20-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="9ce20-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="9ce20-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ce20-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="9ce20-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ce20-132">Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="9ce20-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9ce20-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="9ce20-133">Attributes</span></span>

|<span data-ttu-id="9ce20-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9ce20-134">**Attribute**</span></span>|<span data-ttu-id="9ce20-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ce20-135">**Type**</span></span>|<span data-ttu-id="9ce20-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9ce20-136">**Required**</span></span>|<span data-ttu-id="9ce20-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ce20-137">**Description**</span></span>|<span data-ttu-id="9ce20-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9ce20-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ce20-139">ID</span><span class="sxs-lookup"><span data-stu-id="9ce20-139">ID</span></span>  <br/> |<span data-ttu-id="9ce20-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ce20-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ce20-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ce20-141">required</span></span>  <br/> |<span data-ttu-id="9ce20-142">Gibt den eindeutigen Bezeichner des überprüfungsproblems.</span><span class="sxs-lookup"><span data-stu-id="9ce20-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="9ce20-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ce20-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ce20-144">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="9ce20-144">Ignored</span></span>  <br/> |<span data-ttu-id="9ce20-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9ce20-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ce20-146">Optional</span><span class="sxs-lookup"><span data-stu-id="9ce20-146">optional</span></span>  <br/> |<span data-ttu-id="9ce20-147">Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="9ce20-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="9ce20-148">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="9ce20-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

