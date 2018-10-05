---
title: DataConnection_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389141"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="db5b6-102">DataConnection_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="db5b6-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="db5b6-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="db5b6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db5b6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db5b6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="db5b6-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="db5b6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="db5b6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="db5b6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="db5b6-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="db5b6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="db5b6-108">Keine</span><span class="sxs-lookup"><span data-stu-id="db5b6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db5b6-109">Definition</span><span class="sxs-lookup"><span data-stu-id="db5b6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="db5b6-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="db5b6-110">Elements and attributes</span></span>

<span data-ttu-id="db5b6-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="db5b6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="db5b6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db5b6-112">Child elements</span></span>

<span data-ttu-id="db5b6-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="db5b6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db5b6-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="db5b6-114">Attributes</span></span>

|<span data-ttu-id="db5b6-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="db5b6-115">**Attribute**</span></span>|<span data-ttu-id="db5b6-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="db5b6-116">**Type**</span></span>|<span data-ttu-id="db5b6-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="db5b6-117">**Required**</span></span>|<span data-ttu-id="db5b6-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db5b6-118">**Description**</span></span>|<span data-ttu-id="db5b6-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="db5b6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db5b6-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="db5b6-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="db5b6-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="db5b6-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="db5b6-122">Optional</span><span class="sxs-lookup"><span data-stu-id="db5b6-122">optional</span></span>  <br/> ||<span data-ttu-id="db5b6-123">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="db5b6-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-124">Command</span><span class="sxs-lookup"><span data-stu-id="db5b6-124">Command</span></span>  <br/> |<span data-ttu-id="db5b6-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="db5b6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="db5b6-126">Optional</span><span class="sxs-lookup"><span data-stu-id="db5b6-126">optional</span></span>  <br/> ||<span data-ttu-id="db5b6-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="db5b6-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="db5b6-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="db5b6-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="db5b6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="db5b6-130">Optional</span><span class="sxs-lookup"><span data-stu-id="db5b6-130">optional</span></span>  <br/> ||<span data-ttu-id="db5b6-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="db5b6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-132">FileName</span><span class="sxs-lookup"><span data-stu-id="db5b6-132">FileName</span></span>  <br/> |<span data-ttu-id="db5b6-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="db5b6-133">xsd:string</span></span>  <br/> |<span data-ttu-id="db5b6-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="db5b6-134">required</span></span>  <br/> ||<span data-ttu-id="db5b6-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="db5b6-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="db5b6-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="db5b6-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="db5b6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="db5b6-138">Optional</span><span class="sxs-lookup"><span data-stu-id="db5b6-138">optional</span></span>  <br/> ||<span data-ttu-id="db5b6-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="db5b6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-140">ID</span><span class="sxs-lookup"><span data-stu-id="db5b6-140">ID</span></span>  <br/> |<span data-ttu-id="db5b6-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="db5b6-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db5b6-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="db5b6-142">required</span></span>  <br/> ||<span data-ttu-id="db5b6-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="db5b6-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="db5b6-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="db5b6-144">Timeout</span></span>  <br/> |<span data-ttu-id="db5b6-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="db5b6-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db5b6-146">Optional</span><span class="sxs-lookup"><span data-stu-id="db5b6-146">optional</span></span>  <br/> ||<span data-ttu-id="db5b6-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="db5b6-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

