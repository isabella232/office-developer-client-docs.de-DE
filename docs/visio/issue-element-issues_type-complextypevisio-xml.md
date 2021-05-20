---
title: Issue-Element (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Stellt ein einzelnes Überprüfungsproblem im Dokument dar.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541127"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="d3b63-103">Issue-Element (Issues_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d3b63-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d3b63-104">Stellt ein einzelnes Überprüfungsproblem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="d3b63-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3b63-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d3b63-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3b63-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d3b63-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d3b63-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="d3b63-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d3b63-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d3b63-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d3b63-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d3b63-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d3b63-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d3b63-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d3b63-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="d3b63-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d3b63-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="d3b63-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3b63-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d3b63-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d3b63-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d3b63-114">Elements and attributes</span></span>

<span data-ttu-id="d3b63-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d3b63-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d3b63-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3b63-116">Parent elements</span></span>

|<span data-ttu-id="d3b63-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3b63-117">**Element**</span></span>|<span data-ttu-id="d3b63-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3b63-118">**Type**</span></span>|<span data-ttu-id="d3b63-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3b63-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3b63-120">Issues</span><span class="sxs-lookup"><span data-stu-id="d3b63-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3b63-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="d3b63-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d3b63-122">Enthält alle **Issue-Elemente** für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="d3b63-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d3b63-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3b63-123">Child elements</span></span>

|<span data-ttu-id="d3b63-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3b63-124">**Element**</span></span>|<span data-ttu-id="d3b63-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3b63-125">**Type**</span></span>|<span data-ttu-id="d3b63-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3b63-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3b63-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="d3b63-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3b63-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="d3b63-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d3b63-129">Gibt je nach Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3b63-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="d3b63-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="d3b63-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3b63-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="d3b63-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d3b63-132">Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.</span><span class="sxs-lookup"><span data-stu-id="d3b63-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d3b63-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3b63-133">Attributes</span></span>

|<span data-ttu-id="d3b63-134">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d3b63-134">**Attribute**</span></span>|<span data-ttu-id="d3b63-135">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d3b63-135">**Type**</span></span>|<span data-ttu-id="d3b63-136">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d3b63-136">**Required**</span></span>|<span data-ttu-id="d3b63-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3b63-137">**Description**</span></span>|<span data-ttu-id="d3b63-138">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d3b63-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d3b63-139">ID</span><span class="sxs-lookup"><span data-stu-id="d3b63-139">ID</span></span>  <br/> |<span data-ttu-id="d3b63-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d3b63-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d3b63-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d3b63-141">required</span></span>  <br/> |<span data-ttu-id="d3b63-142">Gibt den eindeutigen Bezeichner des Überprüfungsproblems an.</span><span class="sxs-lookup"><span data-stu-id="d3b63-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="d3b63-143">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d3b63-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d3b63-144">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="d3b63-144">Ignored</span></span>  <br/> |<span data-ttu-id="d3b63-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d3b63-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d3b63-146">Optional</span><span class="sxs-lookup"><span data-stu-id="d3b63-146">optional</span></span>  <br/> |<span data-ttu-id="d3b63-147">Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.</span><span class="sxs-lookup"><span data-stu-id="d3b63-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="d3b63-148">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d3b63-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

