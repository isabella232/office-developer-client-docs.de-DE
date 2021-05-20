---
title: MasterContents-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Gibt Informationen zu den Formen in einem Master in einer Zeichnung an.
ms.openlocfilehash: 26bc86aedeb96544f61f53052ab723b13b29500d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538039"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="119b4-103">MasterContents-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="119b4-103">MasterContents element (Visio XML)</span></span>

<span data-ttu-id="119b4-104">Gibt Informationen zu den Formen in einem Master in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="119b4-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="119b4-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="119b4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="119b4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="119b4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="119b4-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="119b4-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="119b4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="119b4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="119b4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="119b4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="119b4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="119b4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="119b4-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="119b4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="119b4-112">master#.xml</span><span class="sxs-lookup"><span data-stu-id="119b4-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="119b4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="119b4-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="119b4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="119b4-114">Elements and attributes</span></span>

<span data-ttu-id="119b4-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="119b4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="119b4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="119b4-116">Parent elements</span></span>

<span data-ttu-id="119b4-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="119b4-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="119b4-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="119b4-118">Child elements</span></span>

|<span data-ttu-id="119b4-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="119b4-119">**Element**</span></span>|<span data-ttu-id="119b4-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="119b4-120">**Type**</span></span>|<span data-ttu-id="119b4-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="119b4-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="119b4-122">Connects</span><span class="sxs-lookup"><span data-stu-id="119b4-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="119b4-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="119b4-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="119b4-124">Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="119b4-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="119b4-125">Formen</span><span class="sxs-lookup"><span data-stu-id="119b4-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="119b4-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="119b4-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="119b4-127">Enthält eine Auflistung von **Shape-Elementen.**</span><span class="sxs-lookup"><span data-stu-id="119b4-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="119b4-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="119b4-128">Attributes</span></span>

<span data-ttu-id="119b4-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="119b4-129">None.</span></span>
  

