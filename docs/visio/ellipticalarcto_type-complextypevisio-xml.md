---
title: EllipticalArcTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: a6b10c60563a7923990cdb552b1d10fd5c43b97e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345633"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="cddf3-102">EllipticalArcTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cddf3-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cddf3-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="cddf3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cddf3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cddf3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cddf3-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cddf3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cddf3-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cddf3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cddf3-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="cddf3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cddf3-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="cddf3-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cddf3-109">Definition</span><span class="sxs-lookup"><span data-stu-id="cddf3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cddf3-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cddf3-110">Elements and attributes</span></span>

<span data-ttu-id="cddf3-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cddf3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cddf3-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cddf3-112">Child elements</span></span>

|<span data-ttu-id="cddf3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cddf3-113">**Element**</span></span>|<span data-ttu-id="cddf3-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cddf3-114">**Type**</span></span>|<span data-ttu-id="cddf3-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cddf3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cddf3-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cddf3-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="cddf3-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cddf3-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cddf3-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="cddf3-118">Attributes</span></span>

<span data-ttu-id="cddf3-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="cddf3-119">None.</span></span>
  

