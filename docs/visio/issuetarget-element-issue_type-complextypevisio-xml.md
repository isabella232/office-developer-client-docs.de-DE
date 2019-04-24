---
title: IssueTarget-Element (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Hängt vom Ziel des übergeordneten Validierungs Problems ab, ob die Seite oder sowohl die Seite als auch die Form dem übergeordneten Validierungs Problem zugeordnet ist. Wenn das Ziel des übergeordneten Validierungs Problems ein Dokument ist, IssueTarget angibt weder eine Seite noch eine Form.
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332522"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="8853c-104">IssueTarget-Element (Issue_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8853c-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8853c-105">Hängt vom Ziel des übergeordneten Validierungs Problems ab, ob die Seite oder sowohl die Seite als auch die Form dem übergeordneten Validierungs Problem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8853c-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="8853c-106">Wenn das Ziel des übergeordneten Validierungs Problems ein Dokument ist, **IssueTarget** angibt weder eine Seite noch eine Form.</span><span class="sxs-lookup"><span data-stu-id="8853c-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8853c-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8853c-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8853c-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8853c-108">**Element type**</span></span> <br/> |[<span data-ttu-id="8853c-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8853c-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8853c-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8853c-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8853c-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8853c-111">**Schema file**</span></span> <br/> |<span data-ttu-id="8853c-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8853c-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8853c-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="8853c-113">**Document parts**</span></span> <br/> |<span data-ttu-id="8853c-114">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="8853c-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8853c-115">Definition</span><span class="sxs-lookup"><span data-stu-id="8853c-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8853c-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8853c-116">Elements and attributes</span></span>

<span data-ttu-id="8853c-117">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="8853c-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8853c-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8853c-118">Parent elements</span></span>

|<span data-ttu-id="8853c-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8853c-119">**Element**</span></span>|<span data-ttu-id="8853c-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8853c-120">**Type**</span></span>|<span data-ttu-id="8853c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8853c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8853c-122">Problem</span><span class="sxs-lookup"><span data-stu-id="8853c-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8853c-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8853c-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8853c-124">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="8853c-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8853c-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8853c-125">Child elements</span></span>

<span data-ttu-id="8853c-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="8853c-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8853c-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="8853c-127">Attributes</span></span>

|<span data-ttu-id="8853c-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8853c-128">**Attribute**</span></span>|<span data-ttu-id="8853c-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8853c-129">**Type**</span></span>|<span data-ttu-id="8853c-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8853c-130">**Required**</span></span>|<span data-ttu-id="8853c-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8853c-131">**Description**</span></span>|<span data-ttu-id="8853c-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8853c-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8853c-133">PageID</span><span class="sxs-lookup"><span data-stu-id="8853c-133">PageID</span></span>  <br/> |<span data-ttu-id="8853c-134">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8853c-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8853c-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8853c-135">required</span></span>  <br/> |<span data-ttu-id="8853c-136">Gibt den eindeutigen Bezeichner der Seite an, die dem übergeordneten Validierungs Problem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8853c-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="8853c-137">Wenn das Ziel das Dokument ist, kann der Wert der Page-0xFFFFFFFF werden.</span><span class="sxs-lookup"><span data-stu-id="8853c-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="8853c-138">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="8853c-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8853c-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8853c-139">ShapeID</span></span>  <br/> |<span data-ttu-id="8853c-140">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8853c-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8853c-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8853c-141">required</span></span>  <br/> |<span data-ttu-id="8853c-142">Gibt den eindeutigen Bezeichner der Form an, die dem übergeordneten Validierungs Problem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8853c-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="8853c-143">Wenn das Ziel das Dokument oder eine Seite ist, kann der Wert der 0xFFFFFFFF werden.</span><span class="sxs-lookup"><span data-stu-id="8853c-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="8853c-144">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="8853c-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

