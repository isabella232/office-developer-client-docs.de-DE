---
title: Trigger_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541897"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="a5b96-102">Trigger_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a5b96-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a5b96-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a5b96-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5b96-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a5b96-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a5b96-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a5b96-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a5b96-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a5b96-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a5b96-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a5b96-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a5b96-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a5b96-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5b96-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a5b96-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a5b96-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a5b96-110">Elements and attributes</span></span>

<span data-ttu-id="a5b96-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a5b96-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a5b96-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5b96-112">Child elements</span></span>

|<span data-ttu-id="a5b96-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5b96-113">**Element**</span></span>|<span data-ttu-id="a5b96-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a5b96-114">**Type**</span></span>|<span data-ttu-id="a5b96-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5b96-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a5b96-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="a5b96-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a5b96-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a5b96-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a5b96-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5b96-118">Attributes</span></span>

|<span data-ttu-id="a5b96-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a5b96-119">**Attribute**</span></span>|<span data-ttu-id="a5b96-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a5b96-120">**Type**</span></span>|<span data-ttu-id="a5b96-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a5b96-121">**Required**</span></span>|<span data-ttu-id="a5b96-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5b96-122">**Description**</span></span>|<span data-ttu-id="a5b96-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a5b96-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a5b96-124">N</span><span class="sxs-lookup"><span data-stu-id="a5b96-124">N</span></span>  <br/> |<span data-ttu-id="a5b96-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5b96-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a5b96-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a5b96-126">required</span></span>  <br/> ||<span data-ttu-id="a5b96-127">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="a5b96-127">Values of the xsd:string type.</span></span>  <br/> |
   

