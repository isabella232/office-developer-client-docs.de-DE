---
title: MasterContents-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Gibt Informationen zu den Shapes in einem Master-Shape in einer Zeichnung.
ms.openlocfilehash: d1ba67a414ac80be9da2beebb93acc89faf71172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797449"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="f85a7-103">MasterContents-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f85a7-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="f85a7-104">Gibt Informationen zu den Shapes in einem Master-Shape in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="f85a7-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f85a7-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f85a7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f85a7-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f85a7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f85a7-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f85a7-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f85a7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f85a7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f85a7-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f85a7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f85a7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f85a7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f85a7-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="f85a7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f85a7-112">Master-Shape # .xml</span><span class="sxs-lookup"><span data-stu-id="f85a7-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f85a7-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f85a7-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f85a7-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f85a7-114">Elements and attributes</span></span>

<span data-ttu-id="f85a7-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f85a7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f85a7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f85a7-116">Parent elements</span></span>

<span data-ttu-id="f85a7-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="f85a7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f85a7-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f85a7-118">Child elements</span></span>

|<span data-ttu-id="f85a7-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f85a7-119">**Element**</span></span>|<span data-ttu-id="f85a7-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f85a7-120">**Type**</span></span>|<span data-ttu-id="f85a7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f85a7-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f85a7-122">Connects</span><span class="sxs-lookup"><span data-stu-id="f85a7-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f85a7-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="f85a7-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f85a7-124">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="f85a7-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="f85a7-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="f85a7-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f85a7-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f85a7-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f85a7-127">Enthält eine Auflistung von **Shape** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="f85a7-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f85a7-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="f85a7-128">Attributes</span></span>

<span data-ttu-id="f85a7-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="f85a7-129">None.</span></span>
  

