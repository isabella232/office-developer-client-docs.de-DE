---
title: Stellt eine Verbindung her-Element (PageContents_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Enthält ein Connect-Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399956"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="a7942-103">Stellt eine Verbindung her-Element (PageContents_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="a7942-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a7942-104">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="a7942-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a7942-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a7942-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7942-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a7942-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a7942-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="a7942-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a7942-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7942-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a7942-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a7942-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a7942-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a7942-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a7942-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="a7942-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a7942-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="a7942-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7942-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a7942-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7942-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a7942-114">Elements and attributes</span></span>

<span data-ttu-id="a7942-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="a7942-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a7942-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7942-116">Parent elements</span></span>

|<span data-ttu-id="a7942-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7942-117">**Element**</span></span>|<span data-ttu-id="a7942-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a7942-118">**Type**</span></span>|<span data-ttu-id="a7942-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7942-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7942-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="a7942-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="a7942-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="a7942-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7942-122">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="a7942-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="a7942-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="a7942-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="a7942-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="a7942-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7942-125">Gibt die Informationen zu den Shapes in einem Master-Shape oder Zeichenblatt einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="a7942-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7942-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7942-126">Child elements</span></span>

|<span data-ttu-id="a7942-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7942-127">**Element**</span></span>|<span data-ttu-id="a7942-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a7942-128">**Type**</span></span>|<span data-ttu-id="a7942-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7942-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7942-130">Connect</span><span class="sxs-lookup"><span data-stu-id="a7942-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a7942-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="a7942-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7942-132">
			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
</span><span class="sxs-lookup"><span data-stu-id="a7942-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a7942-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7942-133">Attributes</span></span>

<span data-ttu-id="a7942-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7942-134">None.</span></span>
  

