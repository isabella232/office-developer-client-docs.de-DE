---
title: PageContents-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Gibt die Informationen zu den Shapes in einem Master-oder Zeichenblatt einer Zeichnung an.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334510"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="6c501-103">PageContents-Element (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6c501-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="6c501-104">Gibt die Informationen zu den Shapes in einem Master-oder Zeichenblatt einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="6c501-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c501-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6c501-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c501-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6c501-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6c501-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6c501-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6c501-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c501-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6c501-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6c501-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6c501-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6c501-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6c501-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="6c501-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6c501-112">Seite #. XML</span><span class="sxs-lookup"><span data-stu-id="6c501-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c501-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6c501-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c501-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6c501-114">Elements and attributes</span></span>

<span data-ttu-id="6c501-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6c501-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6c501-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c501-116">Parent elements</span></span>

<span data-ttu-id="6c501-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="6c501-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c501-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c501-118">Child elements</span></span>

|<span data-ttu-id="6c501-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c501-119">**Element**</span></span>|<span data-ttu-id="6c501-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6c501-120">**Type**</span></span>|<span data-ttu-id="6c501-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c501-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c501-122">Connects</span><span class="sxs-lookup"><span data-stu-id="6c501-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c501-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="6c501-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6c501-124">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="6c501-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="6c501-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="6c501-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c501-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="6c501-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6c501-127">Gibt eine Auflistung von Formen an.</span><span class="sxs-lookup"><span data-stu-id="6c501-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6c501-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c501-128">Attributes</span></span>

<span data-ttu-id="6c501-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="6c501-129">None.</span></span>
  

