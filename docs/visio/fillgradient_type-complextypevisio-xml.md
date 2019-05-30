---
title: FillGradient_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 83e8eef809f566bb2a69e5b2da1d1c5d932ce54c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539642"
---
# <a name="fillgradienttype-complextype-visio-xml"></a><span data-ttu-id="ac340-102">FillGradient_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ac340-102">FillGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ac340-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ac340-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac340-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac340-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ac340-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ac340-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ac340-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ac340-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ac340-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ac340-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ac340-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ac340-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac340-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ac340-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac340-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ac340-110">Elements and attributes</span></span>

<span data-ttu-id="ac340-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ac340-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ac340-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac340-112">Child elements</span></span>

|<span data-ttu-id="ac340-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac340-113">**Element**</span></span>|<span data-ttu-id="ac340-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ac340-114">**Type**</span></span>|<span data-ttu-id="ac340-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac340-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac340-116">Row</span><span class="sxs-lookup"><span data-stu-id="ac340-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ac340-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="ac340-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ac340-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac340-118">Attributes</span></span>

<span data-ttu-id="ac340-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac340-119">None.</span></span>
  

