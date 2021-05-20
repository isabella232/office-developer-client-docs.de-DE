---
title: DataConnections-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Enthält die DataConnection-Elemente für das Dokument.
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539182"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="e17c1-103">DataConnections-Element (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e17c1-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="e17c1-104">Enthält die **DataConnection-Elemente** für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="e17c1-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e17c1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e17c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e17c1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="e17c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e17c1-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="e17c1-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e17c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e17c1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e17c1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e17c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e17c1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e17c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e17c1-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="e17c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e17c1-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="e17c1-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e17c1-113">Definition</span><span class="sxs-lookup"><span data-stu-id="e17c1-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e17c1-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e17c1-114">Elements and attributes</span></span>

<span data-ttu-id="e17c1-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="e17c1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e17c1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e17c1-116">Parent elements</span></span>

<span data-ttu-id="e17c1-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="e17c1-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e17c1-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e17c1-118">Child elements</span></span>

|<span data-ttu-id="e17c1-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="e17c1-119">**Element**</span></span>|<span data-ttu-id="e17c1-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e17c1-120">**Type**</span></span>|<span data-ttu-id="e17c1-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e17c1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e17c1-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="e17c1-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e17c1-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="e17c1-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e17c1-124">Abstrahiert die Kommunikation zwischen einem oder **mehreren DataRecordset-Elementen** und einer Nicht-XML-Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="e17c1-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e17c1-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="e17c1-125">Attributes</span></span>

|<span data-ttu-id="e17c1-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e17c1-126">**Attribute**</span></span>|<span data-ttu-id="e17c1-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e17c1-127">**Type**</span></span>|<span data-ttu-id="e17c1-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e17c1-128">**Required**</span></span>|<span data-ttu-id="e17c1-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e17c1-129">**Description**</span></span>|<span data-ttu-id="e17c1-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e17c1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e17c1-131">NextID</span><span class="sxs-lookup"><span data-stu-id="e17c1-131">NextID</span></span>  <br/> |<span data-ttu-id="e17c1-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e17c1-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e17c1-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e17c1-133">required</span></span>  <br/> |<span data-ttu-id="e17c1-134">Die nächste verfügbare ID für neue Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="e17c1-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="e17c1-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="e17c1-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

