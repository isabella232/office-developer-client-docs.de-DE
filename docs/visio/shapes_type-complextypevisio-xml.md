---
title: Shapes_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 7d028939ad6c99ecf4160b95764c86779c399c8e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397611"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="e90d5-102">Shapes_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e90d5-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e90d5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e90d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e90d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e90d5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e90d5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e90d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e90d5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e90d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e90d5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e90d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e90d5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="e90d5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e90d5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e90d5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e90d5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e90d5-110">Elements and attributes</span></span>

<span data-ttu-id="e90d5-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e90d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e90d5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e90d5-112">Child elements</span></span>

|<span data-ttu-id="e90d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e90d5-113">**Element**</span></span>|<span data-ttu-id="e90d5-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e90d5-114">**Type**</span></span>|<span data-ttu-id="e90d5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e90d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e90d5-116">Shape</span><span class="sxs-lookup"><span data-stu-id="e90d5-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e90d5-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e90d5-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e90d5-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e90d5-118">Attributes</span></span>

<span data-ttu-id="e90d5-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e90d5-119">None.</span></span>
  

