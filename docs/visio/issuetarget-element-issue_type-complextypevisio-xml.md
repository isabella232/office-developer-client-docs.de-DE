---
title: IssueTarget-Element (Issue_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Je nach das Ziel des übergeordneten gibt Überprüfungsproblem, entweder die Seite oder die Seite und die Form, der übergeordnete Überprüfungsproblem zugeordnet. Wenn das Ziel des überprüfungsproblems der übergeordneten ein Dokument, eine Seite weder ein Shape der IssueTarget angibt.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797273"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="8ba7a-104">IssueTarget-Element (Issue_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8ba7a-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8ba7a-105">Je nach das Ziel des übergeordneten gibt Überprüfungsproblem, entweder die Seite oder die Seite und die Form, der übergeordnete Überprüfungsproblem zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="8ba7a-106">Wenn das Ziel des überprüfungsproblems der übergeordneten ein Dokument, eine Seite weder ein Shape der **IssueTarget** angibt.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8ba7a-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ba7a-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ba7a-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-108">**Element type**</span></span> <br/> |[<span data-ttu-id="8ba7a-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8ba7a-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8ba7a-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8ba7a-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-111">**Schema file**</span></span> <br/> |<span data-ttu-id="8ba7a-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8ba7a-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8ba7a-113">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-113">**Document parts**</span></span> <br/> |<span data-ttu-id="8ba7a-114">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="8ba7a-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ba7a-115">Definition</span><span class="sxs-lookup"><span data-stu-id="8ba7a-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ba7a-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8ba7a-116">Elements and attributes</span></span>

<span data-ttu-id="8ba7a-117">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8ba7a-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba7a-118">Parent elements</span></span>

|<span data-ttu-id="8ba7a-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-119">**Element**</span></span>|<span data-ttu-id="8ba7a-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-120">**Type**</span></span>|<span data-ttu-id="8ba7a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ba7a-122">Problem</span><span class="sxs-lookup"><span data-stu-id="8ba7a-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ba7a-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8ba7a-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ba7a-124">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ba7a-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba7a-125">Child elements</span></span>

<span data-ttu-id="8ba7a-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ba7a-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ba7a-127">Attributes</span></span>

|<span data-ttu-id="8ba7a-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-128">**Attribute**</span></span>|<span data-ttu-id="8ba7a-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-129">**Type**</span></span>|<span data-ttu-id="8ba7a-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-130">**Required**</span></span>|<span data-ttu-id="8ba7a-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-131">**Description**</span></span>|<span data-ttu-id="8ba7a-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8ba7a-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8ba7a-133">PageID</span><span class="sxs-lookup"><span data-stu-id="8ba7a-133">PageID</span></span>  <br/> |<span data-ttu-id="8ba7a-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ba7a-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ba7a-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ba7a-135">required</span></span>  <br/> |<span data-ttu-id="8ba7a-136">Gibt den eindeutigen Bezeichner der Seite, die der übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="8ba7a-137">Wenn das Ziel des Dokuments ist, kann der PageID Wert 0xFFFFFFFF sein.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="8ba7a-138">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8ba7a-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8ba7a-139">ShapeID</span></span>  <br/> |<span data-ttu-id="8ba7a-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8ba7a-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8ba7a-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ba7a-141">required</span></span>  <br/> |<span data-ttu-id="8ba7a-142">Gibt den eindeutigen Bezeichner der Form, die den übergeordneten Überprüfungsproblem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="8ba7a-143">Wenn das Ziel des Dokuments oder einer Seite ist, kann der ShapeID Wert 0xFFFFFFFF sein.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="8ba7a-144">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8ba7a-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

