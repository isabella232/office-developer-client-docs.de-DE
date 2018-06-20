---
title: Probleme-Element (Validation_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Enthält alle Problem Elemente für das Dokument.
ms.openlocfilehash: 9205bf014c81aa699b8bc4a2a7412c5ce59c5fd0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797245"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="a5f26-103">Probleme-Element (Validation_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="a5f26-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a5f26-104">Enthält alle Problem Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="a5f26-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5f26-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a5f26-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5f26-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a5f26-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a5f26-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="a5f26-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a5f26-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a5f26-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a5f26-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a5f26-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a5f26-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a5f26-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a5f26-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="a5f26-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a5f26-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="a5f26-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5f26-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a5f26-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a5f26-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a5f26-114">Elements and attributes</span></span>

<span data-ttu-id="a5f26-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="a5f26-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a5f26-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5f26-116">Parent elements</span></span>

|<span data-ttu-id="a5f26-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5f26-117">**Element**</span></span>|<span data-ttu-id="a5f26-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a5f26-118">**Type**</span></span>|<span data-ttu-id="a5f26-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5f26-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5f26-120">Prüfung</span><span class="sxs-lookup"><span data-stu-id="a5f26-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="a5f26-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a5f26-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a5f26-122">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a5f26-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a5f26-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5f26-123">Child elements</span></span>

|<span data-ttu-id="a5f26-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5f26-124">**Element**</span></span>|<span data-ttu-id="a5f26-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a5f26-125">**Type**</span></span>|<span data-ttu-id="a5f26-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5f26-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5f26-127">Problem</span><span class="sxs-lookup"><span data-stu-id="a5f26-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5f26-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="a5f26-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a5f26-129">Stellt ein einzelnes Überprüfungsproblem im Dokument.</span><span class="sxs-lookup"><span data-stu-id="a5f26-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a5f26-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5f26-130">Attributes</span></span>

<span data-ttu-id="a5f26-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5f26-131">None.</span></span>
  

