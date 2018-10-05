---
title: PageContents-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396568"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="e8292-103">PageContents-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e8292-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="e8292-104">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="e8292-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8292-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e8292-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8292-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="e8292-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e8292-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="e8292-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e8292-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e8292-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e8292-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e8292-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e8292-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e8292-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e8292-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="e8292-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e8292-112">Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="e8292-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8292-113">Definition</span><span class="sxs-lookup"><span data-stu-id="e8292-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e8292-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e8292-114">Elements and attributes</span></span>

<span data-ttu-id="e8292-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e8292-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e8292-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8292-116">Parent elements</span></span>

<span data-ttu-id="e8292-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8292-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8292-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8292-118">Child elements</span></span>

|<span data-ttu-id="e8292-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8292-119">**Element**</span></span>|<span data-ttu-id="e8292-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e8292-120">**Type**</span></span>|<span data-ttu-id="e8292-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8292-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e8292-122">Connects</span><span class="sxs-lookup"><span data-stu-id="e8292-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e8292-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="e8292-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e8292-124">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="e8292-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="e8292-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="e8292-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e8292-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e8292-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e8292-127">Gibt eine Auflistung von Formen.</span><span class="sxs-lookup"><span data-stu-id="e8292-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e8292-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8292-128">Attributes</span></span>

<span data-ttu-id="e8292-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8292-129">None.</span></span>
  

