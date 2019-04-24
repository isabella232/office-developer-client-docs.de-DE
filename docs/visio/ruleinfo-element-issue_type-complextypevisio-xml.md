---
title: RuleInfo-Element (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356987"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="63e64-103">RuleInfo-Element (Issue_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="63e64-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="63e64-104">Gibt Informationen zur Validierungsregel an, für die das übergeordnete Validierungs Problem gilt.</span><span class="sxs-lookup"><span data-stu-id="63e64-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63e64-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="63e64-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63e64-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="63e64-106">**Element type**</span></span> <br/> |[<span data-ttu-id="63e64-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="63e64-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="63e64-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63e64-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="63e64-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="63e64-109">**Schema file**</span></span> <br/> |<span data-ttu-id="63e64-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="63e64-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="63e64-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="63e64-111">**Document parts**</span></span> <br/> |<span data-ttu-id="63e64-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="63e64-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63e64-113">Definition</span><span class="sxs-lookup"><span data-stu-id="63e64-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63e64-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="63e64-114">Elements and attributes</span></span>

<span data-ttu-id="63e64-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="63e64-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="63e64-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63e64-116">Parent elements</span></span>

|<span data-ttu-id="63e64-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="63e64-117">**Element**</span></span>|<span data-ttu-id="63e64-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="63e64-118">**Type**</span></span>|<span data-ttu-id="63e64-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63e64-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63e64-120">Problem</span><span class="sxs-lookup"><span data-stu-id="63e64-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63e64-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="63e64-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63e64-122">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="63e64-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63e64-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63e64-123">Child elements</span></span>

<span data-ttu-id="63e64-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="63e64-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63e64-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="63e64-125">Attributes</span></span>

|<span data-ttu-id="63e64-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="63e64-126">**Attribute**</span></span>|<span data-ttu-id="63e64-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="63e64-127">**Type**</span></span>|<span data-ttu-id="63e64-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="63e64-128">**Required**</span></span>|<span data-ttu-id="63e64-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63e64-129">**Description**</span></span>|<span data-ttu-id="63e64-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="63e64-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63e64-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="63e64-131">RuleID</span></span>  <br/> |<span data-ttu-id="63e64-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63e64-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63e64-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="63e64-133">required</span></span>  <br/> |<span data-ttu-id="63e64-134">Gibt den eindeutigen Bezeichner der Validierungsregel an, zu der das übergeordnete Problem gehört.</span><span class="sxs-lookup"><span data-stu-id="63e64-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="63e64-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="63e64-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63e64-136">Regelsatz</span><span class="sxs-lookup"><span data-stu-id="63e64-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="63e64-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63e64-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63e64-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="63e64-138">required</span></span>  <br/> |<span data-ttu-id="63e64-139">Gibt den eindeutigen Bezeichner des Validierungsregel Satzes an, zu dem das übergeordnete Problem gehört.</span><span class="sxs-lookup"><span data-stu-id="63e64-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="63e64-140">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="63e64-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

