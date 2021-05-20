---
title: PageContents-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537997"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="16e61-103">PageContents-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="16e61-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="16e61-104">Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="16e61-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16e61-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="16e61-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16e61-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="16e61-106">**Element type**</span></span> <br/> |[<span data-ttu-id="16e61-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="16e61-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="16e61-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="16e61-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="16e61-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="16e61-109">**Schema file**</span></span> <br/> |<span data-ttu-id="16e61-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="16e61-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="16e61-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="16e61-111">**Document parts**</span></span> <br/> |<span data-ttu-id="16e61-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="16e61-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16e61-113">Definition</span><span class="sxs-lookup"><span data-stu-id="16e61-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="16e61-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="16e61-114">Elements and attributes</span></span>

<span data-ttu-id="16e61-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="16e61-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="16e61-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16e61-116">Parent elements</span></span>

<span data-ttu-id="16e61-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="16e61-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16e61-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16e61-118">Child elements</span></span>

|<span data-ttu-id="16e61-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="16e61-119">**Element**</span></span>|<span data-ttu-id="16e61-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="16e61-120">**Type**</span></span>|<span data-ttu-id="16e61-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16e61-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16e61-122">Connects</span><span class="sxs-lookup"><span data-stu-id="16e61-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16e61-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="16e61-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16e61-124">Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="16e61-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="16e61-125">Formen</span><span class="sxs-lookup"><span data-stu-id="16e61-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16e61-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="16e61-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="16e61-127">Gibt eine Auflistung von Formen an.</span><span class="sxs-lookup"><span data-stu-id="16e61-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="16e61-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="16e61-128">Attributes</span></span>

<span data-ttu-id="16e61-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="16e61-129">None.</span></span>
  

