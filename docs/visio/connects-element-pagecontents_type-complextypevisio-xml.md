---
title: Connects-Element (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Enthält ein Verbinden-Element für jede Verbindung zwischen zwei Formen in einer Zeichnung.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538711"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="877b9-103">Connects-Element (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="877b9-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="877b9-104">Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="877b9-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="877b9-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="877b9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="877b9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="877b9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="877b9-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="877b9-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="877b9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="877b9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="877b9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="877b9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="877b9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="877b9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="877b9-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="877b9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="877b9-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="877b9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="877b9-113">Definition</span><span class="sxs-lookup"><span data-stu-id="877b9-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="877b9-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="877b9-114">Elements and attributes</span></span>

<span data-ttu-id="877b9-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="877b9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="877b9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="877b9-116">Parent elements</span></span>

|<span data-ttu-id="877b9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="877b9-117">**Element**</span></span>|<span data-ttu-id="877b9-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="877b9-118">**Type**</span></span>|<span data-ttu-id="877b9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="877b9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="877b9-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="877b9-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="877b9-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="877b9-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="877b9-122">Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="877b9-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="877b9-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="877b9-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="877b9-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="877b9-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="877b9-125">Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="877b9-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="877b9-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="877b9-126">Child elements</span></span>

|<span data-ttu-id="877b9-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="877b9-127">**Element**</span></span>|<span data-ttu-id="877b9-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="877b9-128">**Type**</span></span>|<span data-ttu-id="877b9-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="877b9-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="877b9-130">Connect</span><span class="sxs-lookup"><span data-stu-id="877b9-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="877b9-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="877b9-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="877b9-132">Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.</span><span class="sxs-lookup"><span data-stu-id="877b9-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="877b9-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="877b9-133">Attributes</span></span>

<span data-ttu-id="877b9-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="877b9-134">None.</span></span>
  

