---
title: IssueTarget-Element (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Gibt je nach Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten Überprüfungsproblem zugeordnet ist. Wenn das Ziel des übergeordneten Überprüfungsproblems ein Dokument ist, gibt IssueTarget weder eine Seite noch ein Shape an.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542954"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="ddd63-104">IssueTarget-Element (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ddd63-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ddd63-105">Gibt je nach Ziel des übergeordneten Überprüfungsproblems entweder die Seite oder sowohl die Seite als auch die Form an, die dem übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ddd63-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="ddd63-106">Wenn das Ziel des übergeordneten Überprüfungsproblems ein Dokument ist, gibt **IssueTarget** weder eine Seite noch ein Shape an.</span><span class="sxs-lookup"><span data-stu-id="ddd63-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ddd63-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ddd63-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddd63-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ddd63-108">**Element type**</span></span> <br/> |[<span data-ttu-id="ddd63-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="ddd63-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ddd63-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ddd63-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ddd63-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ddd63-111">**Schema file**</span></span> <br/> |<span data-ttu-id="ddd63-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ddd63-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ddd63-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="ddd63-113">**Document parts**</span></span> <br/> |<span data-ttu-id="ddd63-114">validation.xml</span><span class="sxs-lookup"><span data-stu-id="ddd63-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ddd63-115">Definition</span><span class="sxs-lookup"><span data-stu-id="ddd63-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ddd63-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ddd63-116">Elements and attributes</span></span>

<span data-ttu-id="ddd63-117">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ddd63-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ddd63-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddd63-118">Parent elements</span></span>

|<span data-ttu-id="ddd63-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddd63-119">**Element**</span></span>|<span data-ttu-id="ddd63-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ddd63-120">**Type**</span></span>|<span data-ttu-id="ddd63-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddd63-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddd63-122">Problem</span><span class="sxs-lookup"><span data-stu-id="ddd63-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ddd63-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="ddd63-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ddd63-124">Stellt ein einzelnes Überprüfungsproblem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="ddd63-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ddd63-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddd63-125">Child elements</span></span>

<span data-ttu-id="ddd63-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="ddd63-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddd63-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="ddd63-127">Attributes</span></span>

|<span data-ttu-id="ddd63-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ddd63-128">**Attribute**</span></span>|<span data-ttu-id="ddd63-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ddd63-129">**Type**</span></span>|<span data-ttu-id="ddd63-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ddd63-130">**Required**</span></span>|<span data-ttu-id="ddd63-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddd63-131">**Description**</span></span>|<span data-ttu-id="ddd63-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ddd63-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ddd63-133">PageID</span><span class="sxs-lookup"><span data-stu-id="ddd63-133">PageID</span></span>  <br/> |<span data-ttu-id="ddd63-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ddd63-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ddd63-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ddd63-135">required</span></span>  <br/> |<span data-ttu-id="ddd63-136">Gibt den eindeutigen Bezeichner der Seite an, die dem übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ddd63-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="ddd63-137">Wenn das Ziel das Dokument ist, kann der PageID-Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ddd63-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="ddd63-138">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ddd63-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ddd63-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ddd63-139">ShapeID</span></span>  <br/> |<span data-ttu-id="ddd63-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ddd63-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ddd63-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ddd63-141">required</span></span>  <br/> |<span data-ttu-id="ddd63-142">Gibt den eindeutigen Bezeichner des Shapes an, das dem übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ddd63-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="ddd63-143">Wenn das Ziel das Dokument oder eine Seite ist, kann der ShapeID-Wert 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ddd63-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="ddd63-144">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ddd63-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

