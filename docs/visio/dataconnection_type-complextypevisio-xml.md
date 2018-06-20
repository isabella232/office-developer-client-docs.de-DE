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
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="aee39-102">DataConnection_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="aee39-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aee39-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="aee39-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee39-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aee39-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aee39-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="aee39-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aee39-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aee39-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aee39-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="aee39-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aee39-108">Keine</span><span class="sxs-lookup"><span data-stu-id="aee39-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aee39-109">Definition</span><span class="sxs-lookup"><span data-stu-id="aee39-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="aee39-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="aee39-110">Elements and attributes</span></span>

<span data-ttu-id="aee39-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="aee39-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aee39-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aee39-112">Child elements</span></span>

<span data-ttu-id="aee39-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="aee39-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aee39-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="aee39-114">Attributes</span></span>

|<span data-ttu-id="aee39-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aee39-115">**Attribute**</span></span>|<span data-ttu-id="aee39-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aee39-116">**Type**</span></span>|<span data-ttu-id="aee39-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="aee39-117">**Required**</span></span>|<span data-ttu-id="aee39-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aee39-118">**Description**</span></span>|<span data-ttu-id="aee39-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="aee39-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aee39-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="aee39-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="aee39-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="aee39-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aee39-122">Optional</span><span class="sxs-lookup"><span data-stu-id="aee39-122">optional</span></span>  <br/> ||<span data-ttu-id="aee39-123">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="aee39-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aee39-124">Befehl</span><span class="sxs-lookup"><span data-stu-id="aee39-124">Command</span></span>  <br/> |<span data-ttu-id="aee39-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aee39-125">xsd:string</span></span>  <br/> |<span data-ttu-id="aee39-126">Optional</span><span class="sxs-lookup"><span data-stu-id="aee39-126">optional</span></span>  <br/> ||<span data-ttu-id="aee39-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aee39-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aee39-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="aee39-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="aee39-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aee39-129">xsd:string</span></span>  <br/> |<span data-ttu-id="aee39-130">Optional</span><span class="sxs-lookup"><span data-stu-id="aee39-130">optional</span></span>  <br/> ||<span data-ttu-id="aee39-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aee39-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aee39-132">FileName</span><span class="sxs-lookup"><span data-stu-id="aee39-132">FileName</span></span>  <br/> |<span data-ttu-id="aee39-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aee39-133">xsd:string</span></span>  <br/> |<span data-ttu-id="aee39-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="aee39-134">required</span></span>  <br/> ||<span data-ttu-id="aee39-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aee39-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aee39-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="aee39-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="aee39-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="aee39-137">xsd:string</span></span>  <br/> |<span data-ttu-id="aee39-138">Optional</span><span class="sxs-lookup"><span data-stu-id="aee39-138">optional</span></span>  <br/> ||<span data-ttu-id="aee39-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="aee39-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aee39-140">ID</span><span class="sxs-lookup"><span data-stu-id="aee39-140">ID</span></span>  <br/> |<span data-ttu-id="aee39-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aee39-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aee39-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="aee39-142">required</span></span>  <br/> ||<span data-ttu-id="aee39-143">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aee39-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aee39-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="aee39-144">Timeout</span></span>  <br/> |<span data-ttu-id="aee39-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aee39-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aee39-146">Optional</span><span class="sxs-lookup"><span data-stu-id="aee39-146">optional</span></span>  <br/> ||<span data-ttu-id="aee39-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aee39-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

