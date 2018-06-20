---
title: RuleInfo-Element (Issue_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797937"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="d05d1-103">RuleInfo-Element (Issue_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d05d1-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d05d1-104">Gibt Informationen zu der Überprüfungsregel, die für die übergeordnete Überprüfungsproblem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="d05d1-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d05d1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d05d1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d05d1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d05d1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d05d1-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="d05d1-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d05d1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d05d1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d05d1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d05d1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d05d1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d05d1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d05d1-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="d05d1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d05d1-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="d05d1-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d05d1-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d05d1-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d05d1-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d05d1-114">Elements and attributes</span></span>

<span data-ttu-id="d05d1-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d05d1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d05d1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d05d1-116">Parent elements</span></span>

|<span data-ttu-id="d05d1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d05d1-117">**Element**</span></span>|<span data-ttu-id="d05d1-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d05d1-118">**Type**</span></span>|<span data-ttu-id="d05d1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d05d1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d05d1-120">Problem</span><span class="sxs-lookup"><span data-stu-id="d05d1-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d05d1-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="d05d1-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d05d1-122">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="d05d1-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d05d1-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d05d1-123">Child elements</span></span>

<span data-ttu-id="d05d1-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d05d1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d05d1-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d05d1-125">Attributes</span></span>

|<span data-ttu-id="d05d1-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d05d1-126">**Attribute**</span></span>|<span data-ttu-id="d05d1-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d05d1-127">**Type**</span></span>|<span data-ttu-id="d05d1-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d05d1-128">**Required**</span></span>|<span data-ttu-id="d05d1-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d05d1-129">**Description**</span></span>|<span data-ttu-id="d05d1-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d05d1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d05d1-131">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="d05d1-131">RuleID</span></span>  <br/> |<span data-ttu-id="d05d1-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d05d1-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d05d1-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d05d1-133">required</span></span>  <br/> |<span data-ttu-id="d05d1-134">Gibt den eindeutigen Bezeichner der Überprüfungsregel, die für das übergeordnete Problem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="d05d1-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="d05d1-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d05d1-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d05d1-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="d05d1-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="d05d1-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d05d1-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d05d1-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d05d1-138">required</span></span>  <br/> |<span data-ttu-id="d05d1-139">Gibt den eindeutigen Bezeichner der der Überprüfungsregel, die für das übergeordnete Problem relevant ist.</span><span class="sxs-lookup"><span data-stu-id="d05d1-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="d05d1-140">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d05d1-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   
