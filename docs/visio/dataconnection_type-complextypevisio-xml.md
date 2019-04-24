---
title: DataConnection_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344604"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="f5e82-102">DataConnection_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f5e82-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f5e82-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f5e82-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5e82-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f5e82-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f5e82-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f5e82-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f5e82-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f5e82-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f5e82-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f5e82-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f5e82-108">Keine</span><span class="sxs-lookup"><span data-stu-id="f5e82-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5e82-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f5e82-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f5e82-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f5e82-110">Elements and attributes</span></span>

<span data-ttu-id="f5e82-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f5e82-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f5e82-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f5e82-112">Child elements</span></span>

<span data-ttu-id="f5e82-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f5e82-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5e82-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="f5e82-114">Attributes</span></span>

|<span data-ttu-id="f5e82-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f5e82-115">**Attribute**</span></span>|<span data-ttu-id="f5e82-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f5e82-116">**Type**</span></span>|<span data-ttu-id="f5e82-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f5e82-117">**Required**</span></span>|<span data-ttu-id="f5e82-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5e82-118">**Description**</span></span>|<span data-ttu-id="f5e82-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f5e82-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f5e82-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="f5e82-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="f5e82-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f5e82-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5e82-122">Optional</span><span class="sxs-lookup"><span data-stu-id="f5e82-122">optional</span></span>  <br/> ||<span data-ttu-id="f5e82-123">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-124">Befehl</span><span class="sxs-lookup"><span data-stu-id="f5e82-124">Command</span></span>  <br/> |<span data-ttu-id="f5e82-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f5e82-125">xsd:string</span></span>  <br/> |<span data-ttu-id="f5e82-126">Optional</span><span class="sxs-lookup"><span data-stu-id="f5e82-126">optional</span></span>  <br/> ||<span data-ttu-id="f5e82-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f5e82-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="f5e82-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f5e82-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f5e82-130">Optional</span><span class="sxs-lookup"><span data-stu-id="f5e82-130">optional</span></span>  <br/> ||<span data-ttu-id="f5e82-131">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-132">FileName</span><span class="sxs-lookup"><span data-stu-id="f5e82-132">FileName</span></span>  <br/> |<span data-ttu-id="f5e82-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f5e82-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f5e82-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5e82-134">required</span></span>  <br/> ||<span data-ttu-id="f5e82-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5e82-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="f5e82-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f5e82-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f5e82-138">Optional</span><span class="sxs-lookup"><span data-stu-id="f5e82-138">optional</span></span>  <br/> ||<span data-ttu-id="f5e82-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-140">ID</span><span class="sxs-lookup"><span data-stu-id="f5e82-140">ID</span></span>  <br/> |<span data-ttu-id="f5e82-141">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5e82-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5e82-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5e82-142">required</span></span>  <br/> ||<span data-ttu-id="f5e82-143">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5e82-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="f5e82-144">Timeout</span></span>  <br/> |<span data-ttu-id="f5e82-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5e82-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5e82-146">Optional</span><span class="sxs-lookup"><span data-stu-id="f5e82-146">optional</span></span>  <br/> ||<span data-ttu-id="f5e82-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f5e82-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

