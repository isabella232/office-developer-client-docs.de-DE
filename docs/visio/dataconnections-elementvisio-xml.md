---
title: DataConnections-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Enthält die DataConnection-Elemente für das Dokument.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344492"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="fc7b3-103">DataConnections-Element (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="fc7b3-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="fc7b3-104">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fc7b3-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fc7b3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc7b3-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fc7b3-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="fc7b3-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fc7b3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fc7b3-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fc7b3-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fc7b3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fc7b3-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fc7b3-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="fc7b3-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc7b3-113">Definition</span><span class="sxs-lookup"><span data-stu-id="fc7b3-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc7b3-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fc7b3-114">Elements and attributes</span></span>

<span data-ttu-id="fc7b3-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fc7b3-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc7b3-116">Parent elements</span></span>

<span data-ttu-id="fc7b3-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc7b3-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc7b3-118">Child elements</span></span>

|<span data-ttu-id="fc7b3-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-119">**Element**</span></span>|<span data-ttu-id="fc7b3-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-120">**Type**</span></span>|<span data-ttu-id="fc7b3-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc7b3-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="fc7b3-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc7b3-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="fc7b3-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc7b3-124">Abstrahiert die Kommunikation zwischen einem oder mehreren \*\*\*\* DataRecordset-Elementen und einer nicht-XML-Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fc7b3-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="fc7b3-125">Attributes</span></span>

|<span data-ttu-id="fc7b3-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-126">**Attribute**</span></span>|<span data-ttu-id="fc7b3-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-127">**Type**</span></span>|<span data-ttu-id="fc7b3-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-128">**Required**</span></span>|<span data-ttu-id="fc7b3-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-129">**Description**</span></span>|<span data-ttu-id="fc7b3-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fc7b3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fc7b3-131">NextID</span><span class="sxs-lookup"><span data-stu-id="fc7b3-131">NextID</span></span>  <br/> |<span data-ttu-id="fc7b3-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fc7b3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fc7b3-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fc7b3-133">required</span></span>  <br/> |<span data-ttu-id="fc7b3-134">Die nächste verfügbare ID für neue Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="fc7b3-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="fc7b3-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

