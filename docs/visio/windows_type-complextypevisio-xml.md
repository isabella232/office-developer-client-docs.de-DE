---
title: Windows_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 33a2acaad76543115c480b5e9a32ddba8fb0d66a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798415"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="6ef98-102">Windows_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6ef98-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6ef98-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6ef98-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ef98-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ef98-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6ef98-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6ef98-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6ef98-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6ef98-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6ef98-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6ef98-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6ef98-108">Keine</span><span class="sxs-lookup"><span data-stu-id="6ef98-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ef98-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6ef98-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6ef98-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6ef98-110">Elements and attributes</span></span>

<span data-ttu-id="6ef98-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6ef98-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6ef98-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ef98-112">Child elements</span></span>

|<span data-ttu-id="6ef98-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ef98-113">**Element**</span></span>|<span data-ttu-id="6ef98-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6ef98-114">**Type**</span></span>|<span data-ttu-id="6ef98-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ef98-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ef98-116">Window</span><span class="sxs-lookup"><span data-stu-id="6ef98-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ef98-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="6ef98-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6ef98-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ef98-118">Attributes</span></span>

|<span data-ttu-id="6ef98-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6ef98-119">**Attribute**</span></span>|<span data-ttu-id="6ef98-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6ef98-120">**Type**</span></span>|<span data-ttu-id="6ef98-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6ef98-121">**Required**</span></span>|<span data-ttu-id="6ef98-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ef98-122">**Description**</span></span>|<span data-ttu-id="6ef98-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6ef98-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ef98-124">"ClientHeight"</span><span class="sxs-lookup"><span data-stu-id="6ef98-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="6ef98-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6ef98-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6ef98-126">Optional</span><span class="sxs-lookup"><span data-stu-id="6ef98-126">optional</span></span>  <br/> ||<span data-ttu-id="6ef98-127">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6ef98-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6ef98-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="6ef98-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="6ef98-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6ef98-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6ef98-130">Optional</span><span class="sxs-lookup"><span data-stu-id="6ef98-130">optional</span></span>  <br/> ||<span data-ttu-id="6ef98-131">Werte des Typs Xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6ef98-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

