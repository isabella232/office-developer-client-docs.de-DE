---
title: Geometry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 76627f406e8a829a77658cd486b586d8eebd19b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399333"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="c345c-102">Geometry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c345c-102">Geometry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c345c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c345c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c345c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c345c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c345c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c345c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c345c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c345c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c345c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c345c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c345c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c345c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c345c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c345c-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c345c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c345c-110">Elements and attributes</span></span>

<span data-ttu-id="c345c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c345c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c345c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c345c-112">Child elements</span></span>

|<span data-ttu-id="c345c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c345c-113">**Element**</span></span>|<span data-ttu-id="c345c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c345c-114">**Type**</span></span>|<span data-ttu-id="c345c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c345c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c345c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c345c-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c345c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c345c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c345c-118">Row</span><span class="sxs-lookup"><span data-stu-id="c345c-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="c345c-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="c345c-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c345c-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="c345c-120">Attributes</span></span>

<span data-ttu-id="c345c-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="c345c-121">None.</span></span>
  

