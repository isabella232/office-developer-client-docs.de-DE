---
title: DataConnections-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Enthält die DataConnection-Elemente für das Dokument.
ms.openlocfilehash: 4de4429985ab0417341224f7f9e267a9873c6504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796787"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="09c40-103">DataConnections-Element ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="09c40-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="09c40-104">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="09c40-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="09c40-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="09c40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09c40-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="09c40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="09c40-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="09c40-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="09c40-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="09c40-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="09c40-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="09c40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="09c40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="09c40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="09c40-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="09c40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="09c40-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="09c40-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09c40-113">Definition</span><span class="sxs-lookup"><span data-stu-id="09c40-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09c40-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="09c40-114">Elements and attributes</span></span>

<span data-ttu-id="09c40-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="09c40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="09c40-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09c40-116">Parent elements</span></span>

<span data-ttu-id="09c40-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="09c40-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09c40-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09c40-118">Child elements</span></span>

|<span data-ttu-id="09c40-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="09c40-119">**Element**</span></span>|<span data-ttu-id="09c40-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="09c40-120">**Type**</span></span>|<span data-ttu-id="09c40-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09c40-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09c40-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="09c40-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09c40-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="09c40-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09c40-124">Fasst die Kommunikation zwischen einem oder mehreren **DataRecordset** -Elementen und einer nicht auf XML basierenden Datenquelle zusammen.</span><span class="sxs-lookup"><span data-stu-id="09c40-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="09c40-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="09c40-125">Attributes</span></span>

|<span data-ttu-id="09c40-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="09c40-126">**Attribute**</span></span>|<span data-ttu-id="09c40-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="09c40-127">**Type**</span></span>|<span data-ttu-id="09c40-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="09c40-128">**Required**</span></span>|<span data-ttu-id="09c40-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09c40-129">**Description**</span></span>|<span data-ttu-id="09c40-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="09c40-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09c40-131">NextID</span><span class="sxs-lookup"><span data-stu-id="09c40-131">NextID</span></span>  <br/> |<span data-ttu-id="09c40-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09c40-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09c40-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="09c40-133">required</span></span>  <br/> |<span data-ttu-id="09c40-134">Die nächste verfügbare ID für neue Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="09c40-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="09c40-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09c40-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

