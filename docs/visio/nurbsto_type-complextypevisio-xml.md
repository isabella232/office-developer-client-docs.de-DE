---
title: NURBSTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 090df2487eb6fabfba4b3917c7d938fe4f841147
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540917"
---
# <a name="nurbstotype-complextype-visio-xml"></a><span data-ttu-id="2106c-102">NURBSTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2106c-102">NURBSTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2106c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2106c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2106c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2106c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2106c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2106c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2106c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2106c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2106c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2106c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2106c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2106c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2106c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2106c-109">Definition</span></span>

```XML
          <xs:complexType name="NURBSTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2106c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2106c-110">Elements and attributes</span></span>

<span data-ttu-id="2106c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2106c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2106c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2106c-112">Child elements</span></span>

|<span data-ttu-id="2106c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2106c-113">**Element**</span></span>|<span data-ttu-id="2106c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2106c-114">**Type**</span></span>|<span data-ttu-id="2106c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2106c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2106c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2106c-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="2106c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2106c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2106c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="2106c-118">Attributes</span></span>

<span data-ttu-id="2106c-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="2106c-119">None.</span></span>
  

