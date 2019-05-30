---
title: ArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c30c80eb-6327-ebc3-7ea4-8b2fc7525cc0
ms.openlocfilehash: 7fb07f7424e78ffa7b9efec190b839fd7713884a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539698"
---
# <a name="arctotype-complextype-visio-xml"></a><span data-ttu-id="4682f-102">ArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4682f-102">ArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4682f-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="4682f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4682f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4682f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4682f-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4682f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4682f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="4682f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4682f-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="4682f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4682f-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="4682f-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4682f-109">Definition</span><span class="sxs-lookup"><span data-stu-id="4682f-109">Definition</span></span>

```XML
          <xs:complexType name="ArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="4682f-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4682f-110">Elements and attributes</span></span>

<span data-ttu-id="4682f-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4682f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4682f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4682f-112">Child elements</span></span>

|<span data-ttu-id="4682f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4682f-113">**Element**</span></span>|<span data-ttu-id="4682f-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4682f-114">**Type**</span></span>|<span data-ttu-id="4682f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4682f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4682f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="4682f-116">Cell</span></span>](cell-element-arcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="4682f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4682f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4682f-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="4682f-118">Attributes</span></span>

<span data-ttu-id="4682f-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4682f-119">None.</span></span>
  

