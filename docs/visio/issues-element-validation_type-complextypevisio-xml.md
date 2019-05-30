---
title: Issues-Element (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Enthält alle Issue-Elemente für das Dokument.
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542940"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="4f6ec-103">Issues-Element (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4f6ec-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4f6ec-104">Enthält alle Issue-Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f6ec-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4f6ec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f6ec-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f6ec-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="4f6ec-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f6ec-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f6ec-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f6ec-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4f6ec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f6ec-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4f6ec-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="4f6ec-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f6ec-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4f6ec-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f6ec-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4f6ec-114">Elements and attributes</span></span>

<span data-ttu-id="4f6ec-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f6ec-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f6ec-116">Parent elements</span></span>

|<span data-ttu-id="4f6ec-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-117">**Element**</span></span>|<span data-ttu-id="4f6ec-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-118">**Type**</span></span>|<span data-ttu-id="4f6ec-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f6ec-120">Validation</span><span class="sxs-lookup"><span data-stu-id="4f6ec-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f6ec-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="4f6ec-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f6ec-122">Speichert Informationen zur Diagrammüberprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f6ec-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f6ec-123">Child elements</span></span>

|<span data-ttu-id="4f6ec-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-124">**Element**</span></span>|<span data-ttu-id="4f6ec-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-125">**Type**</span></span>|<span data-ttu-id="4f6ec-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f6ec-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f6ec-127">Problem</span><span class="sxs-lookup"><span data-stu-id="4f6ec-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f6ec-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="4f6ec-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f6ec-129">Stellt ein einzelnes Validierungs Problem im Dokument dar.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f6ec-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f6ec-130">Attributes</span></span>

<span data-ttu-id="4f6ec-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-131">None.</span></span>
  

