---
title: Probleme-Element (Validation_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Enthält alle Problem Elemente für das Dokument.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400579"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="b567d-103">Probleme-Element (Validation_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b567d-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b567d-104">Enthält alle Problem Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="b567d-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b567d-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b567d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b567d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b567d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b567d-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b567d-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b567d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b567d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b567d-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b567d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b567d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b567d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b567d-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="b567d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b567d-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="b567d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b567d-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b567d-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b567d-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b567d-114">Elements and attributes</span></span>

<span data-ttu-id="b567d-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b567d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b567d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b567d-116">Parent elements</span></span>

|<span data-ttu-id="b567d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b567d-117">**Element**</span></span>|<span data-ttu-id="b567d-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b567d-118">**Type**</span></span>|<span data-ttu-id="b567d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b567d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b567d-120">Prüfung</span><span class="sxs-lookup"><span data-stu-id="b567d-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="b567d-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="b567d-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b567d-122">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="b567d-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b567d-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b567d-123">Child elements</span></span>

|<span data-ttu-id="b567d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b567d-124">**Element**</span></span>|<span data-ttu-id="b567d-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b567d-125">**Type**</span></span>|<span data-ttu-id="b567d-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b567d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b567d-127">Problem</span><span class="sxs-lookup"><span data-stu-id="b567d-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b567d-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="b567d-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b567d-129">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="b567d-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b567d-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="b567d-130">Attributes</span></span>

<span data-ttu-id="b567d-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="b567d-131">None.</span></span>
  

