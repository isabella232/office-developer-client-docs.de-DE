---
title: RuleSets-Element (Validation_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Enthält ein RuleSet-Element für jeden Überprüfungsregel Satz im Dokument.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319047"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="0c05a-103">RuleSets-Element (Validation_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0c05a-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0c05a-104">Enthält ein **RuleSet** -Element für jeden Überprüfungsregel Satz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="0c05a-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0c05a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0c05a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c05a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="0c05a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0c05a-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="0c05a-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0c05a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0c05a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0c05a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0c05a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0c05a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0c05a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0c05a-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="0c05a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0c05a-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="0c05a-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c05a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="0c05a-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0c05a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0c05a-114">Elements and attributes</span></span>

<span data-ttu-id="0c05a-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="0c05a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0c05a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c05a-116">Parent elements</span></span>

|<span data-ttu-id="0c05a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c05a-117">**Element**</span></span>|<span data-ttu-id="0c05a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0c05a-118">**Type**</span></span>|<span data-ttu-id="0c05a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c05a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c05a-120">Validation</span><span class="sxs-lookup"><span data-stu-id="0c05a-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="0c05a-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="0c05a-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0c05a-122">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0c05a-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0c05a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c05a-123">Child elements</span></span>

|<span data-ttu-id="0c05a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c05a-124">**Element**</span></span>|<span data-ttu-id="0c05a-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0c05a-125">**Type**</span></span>|<span data-ttu-id="0c05a-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c05a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c05a-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="0c05a-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c05a-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="0c05a-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0c05a-129">Stellt einen Satz von Diagramm Validierungsregeln dar.</span><span class="sxs-lookup"><span data-stu-id="0c05a-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0c05a-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c05a-130">Attributes</span></span>

<span data-ttu-id="0c05a-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c05a-131">None.</span></span>
  

