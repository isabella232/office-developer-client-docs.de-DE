---
title: MasterContents-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Gibt Informationen zu den Shapes in einem Master in einer Zeichnung an.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341356"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="66d14-103">MasterContents-Element (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="66d14-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="66d14-104">Gibt Informationen zu den Shapes in einem Master in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="66d14-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="66d14-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66d14-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66d14-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="66d14-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66d14-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="66d14-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66d14-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66d14-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66d14-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="66d14-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66d14-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="66d14-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66d14-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="66d14-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66d14-112">Master #. XML</span><span class="sxs-lookup"><span data-stu-id="66d14-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66d14-113">Definition</span><span class="sxs-lookup"><span data-stu-id="66d14-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66d14-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="66d14-114">Elements and attributes</span></span>

<span data-ttu-id="66d14-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="66d14-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66d14-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66d14-116">Parent elements</span></span>

<span data-ttu-id="66d14-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="66d14-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66d14-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66d14-118">Child elements</span></span>

|<span data-ttu-id="66d14-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="66d14-119">**Element**</span></span>|<span data-ttu-id="66d14-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="66d14-120">**Type**</span></span>|<span data-ttu-id="66d14-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66d14-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66d14-122">Connects</span><span class="sxs-lookup"><span data-stu-id="66d14-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66d14-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="66d14-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66d14-124">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="66d14-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="66d14-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="66d14-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66d14-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="66d14-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66d14-127">Enthält eine Auflistung von **Shape** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="66d14-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66d14-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="66d14-128">Attributes</span></span>

<span data-ttu-id="66d14-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="66d14-129">None.</span></span>
  

