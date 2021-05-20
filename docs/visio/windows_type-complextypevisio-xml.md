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
# <a name="windows_type-complextype-visio-xml"></a><span data-ttu-id="a7aa6-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a7aa6-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a7aa6-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a7aa6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7aa6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a7aa6-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a7aa6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a7aa6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a7aa6-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a7aa6-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a7aa6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7aa6-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a7aa6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a7aa6-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a7aa6-110">Elements and attributes</span></span>

<span data-ttu-id="a7aa6-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a7aa6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7aa6-112">Child elements</span></span>

|<span data-ttu-id="a7aa6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-113">**Element**</span></span>|<span data-ttu-id="a7aa6-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-114">**Type**</span></span>|<span data-ttu-id="a7aa6-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7aa6-116">Window</span><span class="sxs-lookup"><span data-stu-id="a7aa6-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a7aa6-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="a7aa6-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a7aa6-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7aa6-118">Attributes</span></span>

|<span data-ttu-id="a7aa6-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-119">**Attribute**</span></span>|<span data-ttu-id="a7aa6-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-120">**Type**</span></span>|<span data-ttu-id="a7aa6-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-121">**Required**</span></span>|<span data-ttu-id="a7aa6-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-122">**Description**</span></span>|<span data-ttu-id="a7aa6-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a7aa6-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a7aa6-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="a7aa6-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="a7aa6-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a7aa6-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a7aa6-126">Optional</span><span class="sxs-lookup"><span data-stu-id="a7aa6-126">optional</span></span>  <br/> ||<span data-ttu-id="a7aa6-127">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a7aa6-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="a7aa6-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="a7aa6-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a7aa6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a7aa6-130">Optional</span><span class="sxs-lookup"><span data-stu-id="a7aa6-130">optional</span></span>  <br/> ||<span data-ttu-id="a7aa6-131">Werte des Typs xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

