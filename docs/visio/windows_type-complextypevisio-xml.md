---
title: Windows_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538438"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="f1a84-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1a84-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f1a84-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f1a84-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1a84-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1a84-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f1a84-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f1a84-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f1a84-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f1a84-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f1a84-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f1a84-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f1a84-108">Keine</span><span class="sxs-lookup"><span data-stu-id="f1a84-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1a84-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f1a84-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f1a84-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f1a84-110">Elements and attributes</span></span>

<span data-ttu-id="f1a84-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f1a84-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f1a84-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1a84-112">Child elements</span></span>

|<span data-ttu-id="f1a84-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1a84-113">**Element**</span></span>|<span data-ttu-id="f1a84-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f1a84-114">**Type**</span></span>|<span data-ttu-id="f1a84-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1a84-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1a84-116">Window</span><span class="sxs-lookup"><span data-stu-id="f1a84-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1a84-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="f1a84-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f1a84-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1a84-118">Attributes</span></span>

|<span data-ttu-id="f1a84-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f1a84-119">**Attribute**</span></span>|<span data-ttu-id="f1a84-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f1a84-120">**Type**</span></span>|<span data-ttu-id="f1a84-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f1a84-121">**Required**</span></span>|<span data-ttu-id="f1a84-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1a84-122">**Description**</span></span>|<span data-ttu-id="f1a84-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f1a84-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1a84-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="f1a84-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="f1a84-125">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="f1a84-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f1a84-126">Optional</span><span class="sxs-lookup"><span data-stu-id="f1a84-126">optional</span></span>  <br/> ||<span data-ttu-id="f1a84-127">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="f1a84-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f1a84-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="f1a84-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="f1a84-129">XSD: unsignedShort abgeleitet</span><span class="sxs-lookup"><span data-stu-id="f1a84-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f1a84-130">Optional</span><span class="sxs-lookup"><span data-stu-id="f1a84-130">optional</span></span>  <br/> ||<span data-ttu-id="f1a84-131">Werte des XSD: unsignedShort abgeleitet-Typs.</span><span class="sxs-lookup"><span data-stu-id="f1a84-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

