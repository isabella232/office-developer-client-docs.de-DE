---
title: LineTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 15859b84-5486-bb8c-e67e-5d0baaf59ee5
ms.openlocfilehash: 5b6dac15b8c66b4efbe32c22398d577feab47746
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797327"
---
# <a name="linetotype-complextype-visio-xml"></a><span data-ttu-id="b4b56-102">LineTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="b4b56-102">LineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b4b56-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b4b56-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4b56-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4b56-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b4b56-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b4b56-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b4b56-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b4b56-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b4b56-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b4b56-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b4b56-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="b4b56-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4b56-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b4b56-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b4b56-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b4b56-110">Elements and attributes</span></span>

<span data-ttu-id="b4b56-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b4b56-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b4b56-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4b56-112">Child elements</span></span>

|<span data-ttu-id="b4b56-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4b56-113">**Element**</span></span>|<span data-ttu-id="b4b56-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b4b56-114">**Type**</span></span>|<span data-ttu-id="b4b56-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4b56-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4b56-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b4b56-116">Cell</span></span>](cell-element-lineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="b4b56-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b4b56-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b4b56-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4b56-118">Attributes</span></span>

<span data-ttu-id="b4b56-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4b56-119">None.</span></span>
  

