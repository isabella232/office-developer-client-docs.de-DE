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
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="02116-102">DataConnection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02116-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="02116-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="02116-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02116-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02116-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="02116-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="02116-105">**Schema file**</span></span> <br/> |<span data-ttu-id="02116-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="02116-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="02116-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="02116-107">**Extension base**</span></span> <br/> |<span data-ttu-id="02116-108">Keine</span><span class="sxs-lookup"><span data-stu-id="02116-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02116-109">Definition</span><span class="sxs-lookup"><span data-stu-id="02116-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="02116-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="02116-110">Elements and attributes</span></span>

<span data-ttu-id="02116-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="02116-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="02116-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02116-112">Child elements</span></span>

<span data-ttu-id="02116-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="02116-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02116-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="02116-114">Attributes</span></span>

|<span data-ttu-id="02116-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="02116-115">**Attribute**</span></span>|<span data-ttu-id="02116-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="02116-116">**Type**</span></span>|<span data-ttu-id="02116-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="02116-117">**Required**</span></span>|<span data-ttu-id="02116-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02116-118">**Description**</span></span>|<span data-ttu-id="02116-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="02116-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02116-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="02116-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="02116-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="02116-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02116-122">Optional</span><span class="sxs-lookup"><span data-stu-id="02116-122">optional</span></span>  <br/> ||<span data-ttu-id="02116-123">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="02116-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02116-124">Befehl</span><span class="sxs-lookup"><span data-stu-id="02116-124">Command</span></span>  <br/> |<span data-ttu-id="02116-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02116-125">xsd:string</span></span>  <br/> |<span data-ttu-id="02116-126">Optional</span><span class="sxs-lookup"><span data-stu-id="02116-126">optional</span></span>  <br/> ||<span data-ttu-id="02116-127">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="02116-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02116-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="02116-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="02116-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02116-129">xsd:string</span></span>  <br/> |<span data-ttu-id="02116-130">Optional</span><span class="sxs-lookup"><span data-stu-id="02116-130">optional</span></span>  <br/> ||<span data-ttu-id="02116-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="02116-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02116-132">FileName</span><span class="sxs-lookup"><span data-stu-id="02116-132">FileName</span></span>  <br/> |<span data-ttu-id="02116-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02116-133">xsd:string</span></span>  <br/> |<span data-ttu-id="02116-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="02116-134">required</span></span>  <br/> ||<span data-ttu-id="02116-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="02116-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02116-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="02116-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="02116-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="02116-137">xsd:string</span></span>  <br/> |<span data-ttu-id="02116-138">Optional</span><span class="sxs-lookup"><span data-stu-id="02116-138">optional</span></span>  <br/> ||<span data-ttu-id="02116-139">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="02116-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="02116-140">ID</span><span class="sxs-lookup"><span data-stu-id="02116-140">ID</span></span>  <br/> |<span data-ttu-id="02116-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02116-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02116-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="02116-142">required</span></span>  <br/> ||<span data-ttu-id="02116-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="02116-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02116-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="02116-144">Timeout</span></span>  <br/> |<span data-ttu-id="02116-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02116-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02116-146">Optional</span><span class="sxs-lookup"><span data-stu-id="02116-146">optional</span></span>  <br/> ||<span data-ttu-id="02116-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="02116-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

