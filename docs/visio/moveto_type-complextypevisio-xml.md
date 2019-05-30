---
title: MoveTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: 2348d67bb51987efdf2dbb1d9d817b37d754cab9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542660"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="68669-102">MoveTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="68669-102">MoveTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="68669-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="68669-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68669-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68669-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="68669-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="68669-105">**Schema file**</span></span> <br/> |<span data-ttu-id="68669-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="68669-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="68669-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="68669-107">**Extension base**</span></span> <br/> |<span data-ttu-id="68669-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="68669-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68669-109">Definition</span><span class="sxs-lookup"><span data-stu-id="68669-109">Definition</span></span>

```XML
          <xs:complexType name="MoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="68669-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="68669-110">Elements and attributes</span></span>

<span data-ttu-id="68669-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="68669-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="68669-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68669-112">Child elements</span></span>

|<span data-ttu-id="68669-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68669-113">**Element**</span></span>|<span data-ttu-id="68669-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68669-114">**Type**</span></span>|<span data-ttu-id="68669-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68669-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68669-116">Cell</span><span class="sxs-lookup"><span data-stu-id="68669-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="68669-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="68669-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="68669-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="68669-118">Attributes</span></span>

<span data-ttu-id="68669-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="68669-119">None.</span></span>
  

