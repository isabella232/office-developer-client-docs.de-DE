---
title: Windows_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346445"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="102f3-102">Windows_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="102f3-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="102f3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="102f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="102f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="102f3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="102f3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="102f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="102f3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="102f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="102f3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="102f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="102f3-108">Keine</span><span class="sxs-lookup"><span data-stu-id="102f3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="102f3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="102f3-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="102f3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="102f3-110">Elements and attributes</span></span>

<span data-ttu-id="102f3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="102f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="102f3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="102f3-112">Child elements</span></span>

|<span data-ttu-id="102f3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="102f3-113">**Element**</span></span>|<span data-ttu-id="102f3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="102f3-114">**Type**</span></span>|<span data-ttu-id="102f3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="102f3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="102f3-116">Window</span><span class="sxs-lookup"><span data-stu-id="102f3-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="102f3-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="102f3-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="102f3-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="102f3-118">Attributes</span></span>

|<span data-ttu-id="102f3-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="102f3-119">**Attribute**</span></span>|<span data-ttu-id="102f3-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="102f3-120">**Type**</span></span>|<span data-ttu-id="102f3-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="102f3-121">**Required**</span></span>|<span data-ttu-id="102f3-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="102f3-122">**Description**</span></span>|<span data-ttu-id="102f3-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="102f3-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="102f3-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="102f3-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="102f3-125">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="102f3-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="102f3-126">Optional</span><span class="sxs-lookup"><span data-stu-id="102f3-126">optional</span></span>  <br/> ||<span data-ttu-id="102f3-127">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="102f3-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="102f3-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="102f3-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="102f3-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="102f3-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="102f3-130">Optional</span><span class="sxs-lookup"><span data-stu-id="102f3-130">optional</span></span>  <br/> ||<span data-ttu-id="102f3-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="102f3-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

