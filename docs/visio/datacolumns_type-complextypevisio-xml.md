---
title: DataColumns_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: ffe0fbfeaf0b0b67386a6cadd1beb78058819d39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541148"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="ffb3c-102">DataColumns_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ffb3c-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ffb3c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ffb3c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffb3c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ffb3c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ffb3c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ffb3c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ffb3c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ffb3c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ffb3c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ffb3c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ffb3c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ffb3c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ffb3c-110">Elements and attributes</span></span>

<span data-ttu-id="ffb3c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ffb3c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ffb3c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffb3c-112">Child elements</span></span>

|<span data-ttu-id="ffb3c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-113">**Element**</span></span>|<span data-ttu-id="ffb3c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-114">**Type**</span></span>|<span data-ttu-id="ffb3c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ffb3c-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="ffb3c-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ffb3c-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="ffb3c-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ffb3c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffb3c-118">Attributes</span></span>

|<span data-ttu-id="ffb3c-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-119">**Attribute**</span></span>|<span data-ttu-id="ffb3c-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-120">**Type**</span></span>|<span data-ttu-id="ffb3c-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-121">**Required**</span></span>|<span data-ttu-id="ffb3c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-122">**Description**</span></span>|<span data-ttu-id="ffb3c-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ffb3c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ffb3c-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="ffb3c-124">SortAsc</span></span>  <br/> |<span data-ttu-id="ffb3c-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ffb3c-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ffb3c-126">Optional</span><span class="sxs-lookup"><span data-stu-id="ffb3c-126">optional</span></span>  <br/> ||<span data-ttu-id="ffb3c-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ffb3c-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ffb3c-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="ffb3c-128">SortColumn</span></span>  <br/> |<span data-ttu-id="ffb3c-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ffb3c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="ffb3c-130">Optional</span><span class="sxs-lookup"><span data-stu-id="ffb3c-130">optional</span></span>  <br/> ||<span data-ttu-id="ffb3c-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ffb3c-131">Values of the xsd:string type.</span></span>  <br/> |
   

