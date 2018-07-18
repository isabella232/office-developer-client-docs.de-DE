---
title: DataConnection_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 3a900e22fd36c936f689081149b484bd5e7460fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796798"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="764e0-102">DataConnection_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="764e0-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="764e0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="764e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="764e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="764e0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="764e0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="764e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="764e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="764e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="764e0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="764e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="764e0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="764e0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="764e0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="764e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="764e0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="764e0-110">Elements and attributes</span></span>

<span data-ttu-id="764e0-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="764e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="764e0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="764e0-112">Child elements</span></span>

<span data-ttu-id="764e0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="764e0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="764e0-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="764e0-114">Attributes</span></span>

|<span data-ttu-id="764e0-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="764e0-115">**Attribute**</span></span>|<span data-ttu-id="764e0-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="764e0-116">**Type**</span></span>|<span data-ttu-id="764e0-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="764e0-117">**Required**</span></span>|<span data-ttu-id="764e0-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="764e0-118">**Description**</span></span>|<span data-ttu-id="764e0-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="764e0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="764e0-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="764e0-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="764e0-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="764e0-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="764e0-122">Optional</span><span class="sxs-lookup"><span data-stu-id="764e0-122">optional</span></span>  <br/> ||<span data-ttu-id="764e0-123">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="764e0-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="764e0-124">Command</span><span class="sxs-lookup"><span data-stu-id="764e0-124">Command</span></span>  <br/> |<span data-ttu-id="764e0-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="764e0-125">xsd:string</span></span>  <br/> |<span data-ttu-id="764e0-126">Optional</span><span class="sxs-lookup"><span data-stu-id="764e0-126">optional</span></span>  <br/> ||<span data-ttu-id="764e0-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="764e0-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="764e0-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="764e0-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="764e0-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="764e0-129">xsd:string</span></span>  <br/> |<span data-ttu-id="764e0-130">Optional</span><span class="sxs-lookup"><span data-stu-id="764e0-130">optional</span></span>  <br/> ||<span data-ttu-id="764e0-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="764e0-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="764e0-132">FileName</span><span class="sxs-lookup"><span data-stu-id="764e0-132">FileName</span></span>  <br/> |<span data-ttu-id="764e0-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="764e0-133">xsd:string</span></span>  <br/> |<span data-ttu-id="764e0-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="764e0-134">required</span></span>  <br/> ||<span data-ttu-id="764e0-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="764e0-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="764e0-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="764e0-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="764e0-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="764e0-137">xsd:string</span></span>  <br/> |<span data-ttu-id="764e0-138">Optional</span><span class="sxs-lookup"><span data-stu-id="764e0-138">optional</span></span>  <br/> ||<span data-ttu-id="764e0-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="764e0-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="764e0-140">ID</span><span class="sxs-lookup"><span data-stu-id="764e0-140">ID</span></span>  <br/> |<span data-ttu-id="764e0-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="764e0-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="764e0-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="764e0-142">required</span></span>  <br/> ||<span data-ttu-id="764e0-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="764e0-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="764e0-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="764e0-144">Timeout</span></span>  <br/> |<span data-ttu-id="764e0-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="764e0-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="764e0-146">Optional</span><span class="sxs-lookup"><span data-stu-id="764e0-146">optional</span></span>  <br/> ||<span data-ttu-id="764e0-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="764e0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

