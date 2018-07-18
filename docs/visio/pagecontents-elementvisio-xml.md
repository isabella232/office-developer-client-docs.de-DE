---
title: PageContents-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.
ms.openlocfilehash: 0ca705081ad42d799a0155b26eb42ff0b64cd7d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797574"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="8ce46-103">PageContents-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8ce46-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="8ce46-104">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="8ce46-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ce46-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ce46-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ce46-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8ce46-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8ce46-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8ce46-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8ce46-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ce46-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8ce46-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8ce46-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8ce46-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8ce46-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8ce46-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="8ce46-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8ce46-112">Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="8ce46-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ce46-113">Definition</span><span class="sxs-lookup"><span data-stu-id="8ce46-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ce46-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8ce46-114">Elements and attributes</span></span>

<span data-ttu-id="8ce46-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8ce46-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8ce46-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ce46-116">Parent elements</span></span>

<span data-ttu-id="8ce46-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ce46-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ce46-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ce46-118">Child elements</span></span>

|<span data-ttu-id="8ce46-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ce46-119">**Element**</span></span>|<span data-ttu-id="8ce46-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8ce46-120">**Type**</span></span>|<span data-ttu-id="8ce46-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ce46-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ce46-122">Connects</span><span class="sxs-lookup"><span data-stu-id="8ce46-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ce46-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="8ce46-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ce46-124">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="8ce46-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="8ce46-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="8ce46-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ce46-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="8ce46-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ce46-127">Gibt eine Auflistung von Formen.</span><span class="sxs-lookup"><span data-stu-id="8ce46-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8ce46-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ce46-128">Attributes</span></span>

<span data-ttu-id="8ce46-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ce46-129">None.</span></span>
  

