---
title: Shapes_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 707f20823d0413e0b064b2a367da803419889ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798046"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="e831a-102">Shapes_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e831a-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e831a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e831a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e831a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e831a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e831a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e831a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e831a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e831a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e831a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e831a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e831a-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e831a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e831a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e831a-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e831a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e831a-110">Elements and attributes</span></span>

<span data-ttu-id="e831a-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e831a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e831a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e831a-112">Child elements</span></span>

|<span data-ttu-id="e831a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e831a-113">**Element**</span></span>|<span data-ttu-id="e831a-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e831a-114">**Type**</span></span>|<span data-ttu-id="e831a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e831a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e831a-116">Shape</span><span class="sxs-lookup"><span data-stu-id="e831a-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e831a-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e831a-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e831a-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e831a-118">Attributes</span></span>

<span data-ttu-id="e831a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e831a-119">None.</span></span>
  

