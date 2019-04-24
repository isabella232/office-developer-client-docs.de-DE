---
title: Issues-Element (Validation_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Enthält alle Issue-Elemente für das Dokument.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339487"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="646a7-103">Issues-Element (Validation_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="646a7-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="646a7-104">Enthält alle Issue-Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="646a7-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="646a7-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="646a7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="646a7-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="646a7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="646a7-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="646a7-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="646a7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="646a7-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="646a7-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="646a7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="646a7-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="646a7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="646a7-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="646a7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="646a7-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="646a7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="646a7-113">Definition</span><span class="sxs-lookup"><span data-stu-id="646a7-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="646a7-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="646a7-114">Elements and attributes</span></span>

<span data-ttu-id="646a7-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="646a7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="646a7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="646a7-116">Parent elements</span></span>

|<span data-ttu-id="646a7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="646a7-117">**Element**</span></span>|<span data-ttu-id="646a7-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="646a7-118">**Type**</span></span>|<span data-ttu-id="646a7-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="646a7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="646a7-120">Validation</span><span class="sxs-lookup"><span data-stu-id="646a7-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="646a7-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="646a7-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="646a7-122">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="646a7-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="646a7-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="646a7-123">Child elements</span></span>

|<span data-ttu-id="646a7-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="646a7-124">**Element**</span></span>|<span data-ttu-id="646a7-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="646a7-125">**Type**</span></span>|<span data-ttu-id="646a7-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="646a7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="646a7-127">Problem</span><span class="sxs-lookup"><span data-stu-id="646a7-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="646a7-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="646a7-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="646a7-129">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="646a7-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="646a7-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="646a7-130">Attributes</span></span>

<span data-ttu-id="646a7-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="646a7-131">None.</span></span>
  

