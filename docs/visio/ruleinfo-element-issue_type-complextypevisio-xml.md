---
title: RuleInfo-Element (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541687"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="de7f9-103">RuleInfo-Element (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="de7f9-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="de7f9-104">Gibt Informationen zur Überprüfungsregel an, auf die sich das übergeordnete Überprüfungsproblem bezieht.</span><span class="sxs-lookup"><span data-stu-id="de7f9-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de7f9-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="de7f9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de7f9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="de7f9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="de7f9-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="de7f9-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="de7f9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="de7f9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="de7f9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="de7f9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="de7f9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="de7f9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="de7f9-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="de7f9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="de7f9-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="de7f9-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de7f9-113">Definition</span><span class="sxs-lookup"><span data-stu-id="de7f9-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="de7f9-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="de7f9-114">Elements and attributes</span></span>

<span data-ttu-id="de7f9-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="de7f9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="de7f9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de7f9-116">Parent elements</span></span>

|<span data-ttu-id="de7f9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="de7f9-117">**Element**</span></span>|<span data-ttu-id="de7f9-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="de7f9-118">**Type**</span></span>|<span data-ttu-id="de7f9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de7f9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de7f9-120">Problem</span><span class="sxs-lookup"><span data-stu-id="de7f9-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de7f9-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="de7f9-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de7f9-122">Stellt ein einzelnes Überprüfungsproblem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="de7f9-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="de7f9-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de7f9-123">Child elements</span></span>

<span data-ttu-id="de7f9-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="de7f9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de7f9-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="de7f9-125">Attributes</span></span>

|<span data-ttu-id="de7f9-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="de7f9-126">**Attribute**</span></span>|<span data-ttu-id="de7f9-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="de7f9-127">**Type**</span></span>|<span data-ttu-id="de7f9-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="de7f9-128">**Required**</span></span>|<span data-ttu-id="de7f9-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de7f9-129">**Description**</span></span>|<span data-ttu-id="de7f9-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="de7f9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="de7f9-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="de7f9-131">RuleID</span></span>  <br/> |<span data-ttu-id="de7f9-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="de7f9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="de7f9-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="de7f9-133">required</span></span>  <br/> |<span data-ttu-id="de7f9-134">Gibt den eindeutigen Bezeichner der Gültigkeitsprüfungsregel an, auf die sich das übergeordnete Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="de7f9-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="de7f9-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="de7f9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="de7f9-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="de7f9-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="de7f9-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="de7f9-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="de7f9-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="de7f9-138">required</span></span>  <br/> |<span data-ttu-id="de7f9-139">Gibt den eindeutigen Bezeichner des Überprüfungsregelsatzs an, auf den sich das übergeordnete Problem bezieht.</span><span class="sxs-lookup"><span data-stu-id="de7f9-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="de7f9-140">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="de7f9-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

