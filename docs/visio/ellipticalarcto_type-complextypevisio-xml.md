---
title: EllipticalArcTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: a6b10c60563a7923990cdb552b1d10fd5c43b97e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397254"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="0c2d7-102">EllipticalArcTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0c2d7-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0c2d7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0c2d7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c2d7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c2d7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c2d7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c2d7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c2d7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c2d7-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="0c2d7-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c2d7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0c2d7-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0c2d7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0c2d7-110">Elements and attributes</span></span>

<span data-ttu-id="0c2d7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0c2d7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c2d7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c2d7-112">Child elements</span></span>

|<span data-ttu-id="0c2d7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-113">**Element**</span></span>|<span data-ttu-id="0c2d7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-114">**Type**</span></span>|<span data-ttu-id="0c2d7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c2d7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c2d7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0c2d7-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="0c2d7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0c2d7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0c2d7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c2d7-118">Attributes</span></span>

<span data-ttu-id="0c2d7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c2d7-119">None.</span></span>
  

