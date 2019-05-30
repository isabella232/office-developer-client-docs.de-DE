---
title: Issue-Element (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Validierungs Problem im Dokument dar.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541127"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="b8c31-103">Issue-Element (Issues_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b8c31-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b8c31-104">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="b8c31-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8c31-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b8c31-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8c31-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b8c31-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b8c31-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="b8c31-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b8c31-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b8c31-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b8c31-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b8c31-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b8c31-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b8c31-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b8c31-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="b8c31-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b8c31-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="b8c31-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8c31-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b8c31-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8c31-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b8c31-114">Elements and attributes</span></span>

<span data-ttu-id="b8c31-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b8c31-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b8c31-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8c31-116">Parent elements</span></span>

|<span data-ttu-id="b8c31-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8c31-117">**Element**</span></span>|<span data-ttu-id="b8c31-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b8c31-118">**Type**</span></span>|<span data-ttu-id="b8c31-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8c31-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8c31-120">Issues</span><span class="sxs-lookup"><span data-stu-id="b8c31-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8c31-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b8c31-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8c31-122">Enthält alle **Issue** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="b8c31-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b8c31-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8c31-123">Child elements</span></span>

|<span data-ttu-id="b8c31-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8c31-124">**Element**</span></span>|<span data-ttu-id="b8c31-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b8c31-125">**Type**</span></span>|<span data-ttu-id="b8c31-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8c31-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8c31-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="b8c31-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8c31-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="b8c31-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8c31-129">Gibt je nach Ziel des übergeordneten Überprüfungs Problems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8c31-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="b8c31-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="b8c31-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8c31-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="b8c31-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8c31-132">Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Validierungs Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="b8c31-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b8c31-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8c31-133">Attributes</span></span>

|<span data-ttu-id="b8c31-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b8c31-134">**Attribute**</span></span>|<span data-ttu-id="b8c31-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b8c31-135">**Type**</span></span>|<span data-ttu-id="b8c31-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b8c31-136">**Required**</span></span>|<span data-ttu-id="b8c31-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8c31-137">**Description**</span></span>|<span data-ttu-id="b8c31-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b8c31-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8c31-139">ID</span><span class="sxs-lookup"><span data-stu-id="b8c31-139">ID</span></span>  <br/> |<span data-ttu-id="b8c31-140">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b8c31-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b8c31-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b8c31-141">required</span></span>  <br/> |<span data-ttu-id="b8c31-142">Gibt den eindeutigen Bezeichner des Überprüfungs Problems an.</span><span class="sxs-lookup"><span data-stu-id="b8c31-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="b8c31-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b8c31-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b8c31-144">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="b8c31-144">Ignored</span></span>  <br/> |<span data-ttu-id="b8c31-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="b8c31-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b8c31-146">Optional</span><span class="sxs-lookup"><span data-stu-id="b8c31-146">optional</span></span>  <br/> |<span data-ttu-id="b8c31-147">Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Validierungs Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="b8c31-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="b8c31-148">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="b8c31-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

