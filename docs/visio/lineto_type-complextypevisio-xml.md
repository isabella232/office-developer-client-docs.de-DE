---
title: LineTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 15859b84-5486-bb8c-e67e-5d0baaf59ee5
ms.openlocfilehash: 90d85002763f11d3bda27d41be6428824a5f0a21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537787"
---
# <a name="linetotype-complextype-visio-xml"></a><span data-ttu-id="56e7b-102">LineTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="56e7b-102">LineTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="56e7b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="56e7b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56e7b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="56e7b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="56e7b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="56e7b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="56e7b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="56e7b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="56e7b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="56e7b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="56e7b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="56e7b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56e7b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="56e7b-109">Definition</span></span>

```XML
          <xs:complexType name="LineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="56e7b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="56e7b-110">Elements and attributes</span></span>

<span data-ttu-id="56e7b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="56e7b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="56e7b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56e7b-112">Child elements</span></span>

|<span data-ttu-id="56e7b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="56e7b-113">**Element**</span></span>|<span data-ttu-id="56e7b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="56e7b-114">**Type**</span></span>|<span data-ttu-id="56e7b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56e7b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56e7b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="56e7b-116">Cell</span></span>](cell-element-lineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="56e7b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="56e7b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="56e7b-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="56e7b-118">Attributes</span></span>

<span data-ttu-id="56e7b-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="56e7b-119">None.</span></span>
  

