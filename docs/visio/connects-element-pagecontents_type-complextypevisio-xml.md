---
title: Stellt eine Verbindung her-Element (PageContents_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Enthält ein Connect-Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796722"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="afd18-103">Stellt eine Verbindung her-Element (PageContents_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="afd18-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="afd18-104">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="afd18-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="afd18-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="afd18-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afd18-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="afd18-106">**Element type**</span></span> <br/> |[<span data-ttu-id="afd18-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="afd18-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="afd18-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="afd18-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="afd18-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="afd18-109">**Schema file**</span></span> <br/> |<span data-ttu-id="afd18-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="afd18-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="afd18-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="afd18-111">**Document parts**</span></span> <br/> |<span data-ttu-id="afd18-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="afd18-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="afd18-113">Definition</span><span class="sxs-lookup"><span data-stu-id="afd18-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="afd18-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="afd18-114">Elements and attributes</span></span>

<span data-ttu-id="afd18-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="afd18-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="afd18-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afd18-116">Parent elements</span></span>

|<span data-ttu-id="afd18-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="afd18-117">**Element**</span></span>|<span data-ttu-id="afd18-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="afd18-118">**Type**</span></span>|<span data-ttu-id="afd18-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afd18-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afd18-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="afd18-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="afd18-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="afd18-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afd18-122">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="afd18-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="afd18-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="afd18-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="afd18-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="afd18-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afd18-125">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="afd18-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afd18-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afd18-126">Child elements</span></span>

|<span data-ttu-id="afd18-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="afd18-127">**Element**</span></span>|<span data-ttu-id="afd18-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="afd18-128">**Type**</span></span>|<span data-ttu-id="afd18-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afd18-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afd18-130">Connect</span><span class="sxs-lookup"><span data-stu-id="afd18-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="afd18-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="afd18-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afd18-132">
			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
</span><span class="sxs-lookup"><span data-stu-id="afd18-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="afd18-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="afd18-133">Attributes</span></span>

<span data-ttu-id="afd18-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="afd18-134">None.</span></span>
  

