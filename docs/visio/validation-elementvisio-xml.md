---
title: Validation-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Speichert Informationen zur Diagrammüberprüfung des Dokuments.
ms.openlocfilehash: f4a7c0893baebb09dccd743c3006a5512dec533d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798367"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="5a3b5-103">Validation-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="5a3b5-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="5a3b5-104">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a3b5-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5a3b5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a3b5-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5a3b5-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="5a3b5-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5a3b5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5a3b5-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5a3b5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5a3b5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5a3b5-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5a3b5-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="5a3b5-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5a3b5-113">Definition</span><span class="sxs-lookup"><span data-stu-id="5a3b5-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5a3b5-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5a3b5-114">Elements and attributes</span></span>

<span data-ttu-id="5a3b5-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5a3b5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a3b5-116">Parent elements</span></span>

<span data-ttu-id="5a3b5-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a3b5-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a3b5-118">Child elements</span></span>

|<span data-ttu-id="5a3b5-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-119">**Element**</span></span>|<span data-ttu-id="5a3b5-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-120">**Type**</span></span>|<span data-ttu-id="5a3b5-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a3b5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5a3b5-122">Probleme</span><span class="sxs-lookup"><span data-stu-id="5a3b5-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5a3b5-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5a3b5-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5a3b5-124">Enthält alle **Problem** Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="5a3b5-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="5a3b5-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5a3b5-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="5a3b5-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5a3b5-127">Enthält ein **RuleSet** -Element für jeden überprüfungsregelsatz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="5a3b5-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="5a3b5-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5a3b5-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="5a3b5-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5a3b5-130">Die Eigenschaften, die im Zusammenhang mit dem Dokument Validierung kapselt.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5a3b5-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a3b5-131">Attributes</span></span>

<span data-ttu-id="5a3b5-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="5a3b5-132">None.</span></span>
  

