---
title: Validation-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Speichert Informationen zur Diagrammüberprüfung des Dokuments.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329084"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="a7aea-103">Validation-Element (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a7aea-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="a7aea-104">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a7aea-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7aea-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a7aea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7aea-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a7aea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a7aea-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a7aea-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a7aea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7aea-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a7aea-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a7aea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a7aea-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a7aea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a7aea-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="a7aea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a7aea-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="a7aea-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7aea-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a7aea-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7aea-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a7aea-114">Elements and attributes</span></span>

<span data-ttu-id="a7aea-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a7aea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a7aea-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7aea-116">Parent elements</span></span>

<span data-ttu-id="a7aea-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7aea-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7aea-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7aea-118">Child elements</span></span>

|<span data-ttu-id="a7aea-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7aea-119">**Element**</span></span>|<span data-ttu-id="a7aea-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a7aea-120">**Type**</span></span>|<span data-ttu-id="a7aea-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7aea-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7aea-122">Issues</span><span class="sxs-lookup"><span data-stu-id="a7aea-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a7aea-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="a7aea-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7aea-124">Enthält alle **Issue** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="a7aea-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="a7aea-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="a7aea-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a7aea-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="a7aea-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7aea-127">Enthält ein **RuleSet** -Element für jeden Überprüfungsregel Satz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="a7aea-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="a7aea-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="a7aea-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a7aea-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="a7aea-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7aea-130">Kapselt die Eigenschaften, die im Zusammenhang mit der Validierung des Dokuments stehen.</span><span class="sxs-lookup"><span data-stu-id="a7aea-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a7aea-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7aea-131">Attributes</span></span>

<span data-ttu-id="a7aea-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7aea-132">None.</span></span>
  

