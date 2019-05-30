---
title: RelQuadBezTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 558c7315-5025-484b-446e-333890bc1c3a
ms.openlocfilehash: c91532517794e4d1882acd5fd1679e4152a54534
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542737"
---
# <a name="relquadbeztotype-complextype-visio-xml"></a><span data-ttu-id="80d3a-102">RelQuadBezTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="80d3a-102">RelQuadBezTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="80d3a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="80d3a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80d3a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80d3a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="80d3a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="80d3a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="80d3a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="80d3a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="80d3a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="80d3a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="80d3a-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="80d3a-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80d3a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="80d3a-109">Definition</span></span>

```XML
          <xs:complexType name="RelQuadBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="80d3a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="80d3a-110">Elements and attributes</span></span>

<span data-ttu-id="80d3a-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="80d3a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="80d3a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80d3a-112">Child elements</span></span>

|<span data-ttu-id="80d3a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="80d3a-113">**Element**</span></span>|<span data-ttu-id="80d3a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="80d3a-114">**Type**</span></span>|<span data-ttu-id="80d3a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80d3a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80d3a-116">Cell</span><span class="sxs-lookup"><span data-stu-id="80d3a-116">Cell</span></span>](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="80d3a-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="80d3a-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="80d3a-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="80d3a-118">Attributes</span></span>

<span data-ttu-id="80d3a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="80d3a-119">None.</span></span>
  

