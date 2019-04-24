---
title: Issue-Element (Issues_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Validierungs Problem im Dokument dar.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317906"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="68657-103">Issue-Element (Issues_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="68657-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="68657-104">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="68657-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68657-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68657-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68657-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="68657-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68657-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="68657-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68657-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68657-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68657-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="68657-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68657-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="68657-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68657-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="68657-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68657-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="68657-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68657-113">Definition</span><span class="sxs-lookup"><span data-stu-id="68657-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68657-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="68657-114">Elements and attributes</span></span>

<span data-ttu-id="68657-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="68657-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68657-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68657-116">Parent elements</span></span>

|<span data-ttu-id="68657-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="68657-117">**Element**</span></span>|<span data-ttu-id="68657-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68657-118">**Type**</span></span>|<span data-ttu-id="68657-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68657-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68657-120">Issues</span><span class="sxs-lookup"><span data-stu-id="68657-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68657-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="68657-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68657-122">Enthält alle **Issue** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="68657-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68657-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68657-123">Child elements</span></span>

|<span data-ttu-id="68657-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="68657-124">**Element**</span></span>|<span data-ttu-id="68657-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68657-125">**Type**</span></span>|<span data-ttu-id="68657-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68657-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68657-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="68657-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68657-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="68657-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68657-129">Hängt vom Ziel des übergeordneten Validierungs Problems ab, ob die Seite oder sowohl die Seite als auch die Form dem übergeordneten Validierungs Problem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68657-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="68657-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="68657-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68657-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="68657-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68657-132">Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.</span><span class="sxs-lookup"><span data-stu-id="68657-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68657-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="68657-133">Attributes</span></span>

|<span data-ttu-id="68657-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68657-134">**Attribute**</span></span>|<span data-ttu-id="68657-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68657-135">**Type**</span></span>|<span data-ttu-id="68657-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="68657-136">**Required**</span></span>|<span data-ttu-id="68657-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68657-137">**Description**</span></span>|<span data-ttu-id="68657-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="68657-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68657-139">ID</span><span class="sxs-lookup"><span data-stu-id="68657-139">ID</span></span>  <br/> |<span data-ttu-id="68657-140">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68657-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68657-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="68657-141">required</span></span>  <br/> |<span data-ttu-id="68657-142">Gibt den eindeutigen Bezeichner des Validierungs Problems an.</span><span class="sxs-lookup"><span data-stu-id="68657-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="68657-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="68657-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68657-144">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="68657-144">Ignored</span></span>  <br/> |<span data-ttu-id="68657-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="68657-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="68657-146">Optional</span><span class="sxs-lookup"><span data-stu-id="68657-146">optional</span></span>  <br/> |<span data-ttu-id="68657-147">Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.</span><span class="sxs-lookup"><span data-stu-id="68657-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="68657-148">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="68657-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

