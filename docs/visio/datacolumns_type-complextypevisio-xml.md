---
title: DataColumns_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796781"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="92322-102">DataColumns_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="92322-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="92322-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="92322-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92322-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92322-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92322-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="92322-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92322-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="92322-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92322-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="92322-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92322-108">Keine</span><span class="sxs-lookup"><span data-stu-id="92322-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92322-109">Definition</span><span class="sxs-lookup"><span data-stu-id="92322-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92322-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="92322-110">Elements and attributes</span></span>

<span data-ttu-id="92322-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="92322-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92322-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92322-112">Child elements</span></span>

|<span data-ttu-id="92322-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="92322-113">**Element**</span></span>|<span data-ttu-id="92322-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92322-114">**Type**</span></span>|<span data-ttu-id="92322-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92322-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92322-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="92322-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92322-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="92322-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="92322-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="92322-118">Attributes</span></span>

|<span data-ttu-id="92322-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92322-119">**Attribute**</span></span>|<span data-ttu-id="92322-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92322-120">**Type**</span></span>|<span data-ttu-id="92322-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="92322-121">**Required**</span></span>|<span data-ttu-id="92322-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92322-122">**Description**</span></span>|<span data-ttu-id="92322-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="92322-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92322-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="92322-124">SortAsc</span></span>  <br/> |<span data-ttu-id="92322-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="92322-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92322-126">Optional</span><span class="sxs-lookup"><span data-stu-id="92322-126">optional</span></span>  <br/> ||<span data-ttu-id="92322-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="92322-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92322-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="92322-128">SortColumn</span></span>  <br/> |<span data-ttu-id="92322-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="92322-129">xsd:string</span></span>  <br/> |<span data-ttu-id="92322-130">Optional</span><span class="sxs-lookup"><span data-stu-id="92322-130">optional</span></span>  <br/> ||<span data-ttu-id="92322-131">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="92322-131">Values of the xsd:string type.</span></span>  <br/> |
   

