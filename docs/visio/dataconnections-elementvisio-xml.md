---
title: DataConnections-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Enthält die DataConnection-Elemente für das Dokument.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395028"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="d15de-103">DataConnections-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d15de-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="d15de-104">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="d15de-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d15de-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d15de-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d15de-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d15de-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d15de-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="d15de-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d15de-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d15de-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d15de-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d15de-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d15de-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d15de-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d15de-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="d15de-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d15de-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="d15de-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d15de-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d15de-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d15de-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d15de-114">Elements and attributes</span></span>

<span data-ttu-id="d15de-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d15de-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d15de-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d15de-116">Parent elements</span></span>

<span data-ttu-id="d15de-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="d15de-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d15de-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d15de-118">Child elements</span></span>

|<span data-ttu-id="d15de-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="d15de-119">**Element**</span></span>|<span data-ttu-id="d15de-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d15de-120">**Type**</span></span>|<span data-ttu-id="d15de-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d15de-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d15de-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="d15de-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d15de-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="d15de-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d15de-124">Fasst die Kommunikation zwischen einem oder mehreren **DataRecordset** -Elementen und einer nicht auf XML basierenden Datenquelle zusammen.</span><span class="sxs-lookup"><span data-stu-id="d15de-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d15de-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d15de-125">Attributes</span></span>

|<span data-ttu-id="d15de-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d15de-126">**Attribute**</span></span>|<span data-ttu-id="d15de-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d15de-127">**Type**</span></span>|<span data-ttu-id="d15de-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d15de-128">**Required**</span></span>|<span data-ttu-id="d15de-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d15de-129">**Description**</span></span>|<span data-ttu-id="d15de-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d15de-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d15de-131">NextID</span><span class="sxs-lookup"><span data-stu-id="d15de-131">NextID</span></span>  <br/> |<span data-ttu-id="d15de-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d15de-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d15de-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d15de-133">required</span></span>  <br/> |<span data-ttu-id="d15de-134">Die nächste verfügbare ID für neue Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="d15de-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="d15de-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d15de-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

