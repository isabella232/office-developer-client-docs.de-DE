---
title: Validation-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Speichert Informationen zur Diagrammüberprüfung des Dokuments.
ms.openlocfilehash: b1b1bcbd70d57d7a7316e91d137cf8c3c3750722
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538550"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="b03cd-103">Validation-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b03cd-103">Validation element (Visio XML)</span></span>

<span data-ttu-id="b03cd-104">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="b03cd-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b03cd-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b03cd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b03cd-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b03cd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b03cd-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="b03cd-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b03cd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b03cd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b03cd-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b03cd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b03cd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b03cd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b03cd-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="b03cd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b03cd-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="b03cd-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b03cd-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b03cd-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b03cd-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b03cd-114">Elements and attributes</span></span>

<span data-ttu-id="b03cd-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b03cd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b03cd-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b03cd-116">Parent elements</span></span>

<span data-ttu-id="b03cd-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="b03cd-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b03cd-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b03cd-118">Child elements</span></span>

|<span data-ttu-id="b03cd-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="b03cd-119">**Element**</span></span>|<span data-ttu-id="b03cd-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b03cd-120">**Type**</span></span>|<span data-ttu-id="b03cd-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b03cd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b03cd-122">Issues</span><span class="sxs-lookup"><span data-stu-id="b03cd-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b03cd-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b03cd-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b03cd-124">Enthält alle **Issue-Elemente** für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="b03cd-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="b03cd-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="b03cd-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b03cd-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="b03cd-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b03cd-127">Enthält ein **RuleSet-Element** für jeden Überprüfungsregelsatz im Dokument.</span><span class="sxs-lookup"><span data-stu-id="b03cd-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="b03cd-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="b03cd-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b03cd-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="b03cd-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b03cd-130">Kapselt die Eigenschaften, die im Zusammenhang mit der Überprüfung des Dokuments stehen.</span><span class="sxs-lookup"><span data-stu-id="b03cd-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b03cd-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="b03cd-131">Attributes</span></span>

<span data-ttu-id="b03cd-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="b03cd-132">None.</span></span>
  

