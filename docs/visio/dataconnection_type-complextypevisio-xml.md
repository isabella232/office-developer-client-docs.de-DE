---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539649"
---
# <a name="dataconnection_type-complextype-visio-xml"></a><span data-ttu-id="71f56-102">DataConnection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="71f56-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="71f56-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="71f56-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71f56-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="71f56-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="71f56-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="71f56-105">**Schema file**</span></span> <br/> |<span data-ttu-id="71f56-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="71f56-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="71f56-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="71f56-107">**Extension base**</span></span> <br/> |<span data-ttu-id="71f56-108">Keine</span><span class="sxs-lookup"><span data-stu-id="71f56-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71f56-109">Definition</span><span class="sxs-lookup"><span data-stu-id="71f56-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71f56-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="71f56-110">Elements and attributes</span></span>

<span data-ttu-id="71f56-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="71f56-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="71f56-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71f56-112">Child elements</span></span>

<span data-ttu-id="71f56-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="71f56-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71f56-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="71f56-114">Attributes</span></span>

|<span data-ttu-id="71f56-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="71f56-115">**Attribute**</span></span>|<span data-ttu-id="71f56-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="71f56-116">**Type**</span></span>|<span data-ttu-id="71f56-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="71f56-117">**Required**</span></span>|<span data-ttu-id="71f56-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71f56-118">**Description**</span></span>|<span data-ttu-id="71f56-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="71f56-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="71f56-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="71f56-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="71f56-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="71f56-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="71f56-122">Optional</span><span class="sxs-lookup"><span data-stu-id="71f56-122">optional</span></span>  <br/> ||<span data-ttu-id="71f56-123">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="71f56-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="71f56-124">Get-Help</span><span class="sxs-lookup"><span data-stu-id="71f56-124">Command</span></span>  <br/> |<span data-ttu-id="71f56-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="71f56-125">xsd:string</span></span>  <br/> |<span data-ttu-id="71f56-126">Optional</span><span class="sxs-lookup"><span data-stu-id="71f56-126">optional</span></span>  <br/> ||<span data-ttu-id="71f56-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71f56-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="71f56-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="71f56-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="71f56-129">xsd:string</span></span>  <br/> |<span data-ttu-id="71f56-130">Optional</span><span class="sxs-lookup"><span data-stu-id="71f56-130">optional</span></span>  <br/> ||<span data-ttu-id="71f56-131">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71f56-132">FileName</span><span class="sxs-lookup"><span data-stu-id="71f56-132">FileName</span></span>  <br/> |<span data-ttu-id="71f56-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="71f56-133">xsd:string</span></span>  <br/> |<span data-ttu-id="71f56-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="71f56-134">required</span></span>  <br/> ||<span data-ttu-id="71f56-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71f56-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="71f56-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="71f56-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="71f56-137">xsd:string</span></span>  <br/> |<span data-ttu-id="71f56-138">Optional</span><span class="sxs-lookup"><span data-stu-id="71f56-138">optional</span></span>  <br/> ||<span data-ttu-id="71f56-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="71f56-140">ID</span><span class="sxs-lookup"><span data-stu-id="71f56-140">ID</span></span>  <br/> |<span data-ttu-id="71f56-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="71f56-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="71f56-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="71f56-142">required</span></span>  <br/> ||<span data-ttu-id="71f56-143">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="71f56-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="71f56-144">Timeout</span></span>  <br/> |<span data-ttu-id="71f56-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="71f56-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="71f56-146">Optional</span><span class="sxs-lookup"><span data-stu-id="71f56-146">optional</span></span>  <br/> ||<span data-ttu-id="71f56-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="71f56-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

