---
title: SplineStart_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4395e39c-51bb-b232-bd8a-c5e53ae95169
ms.openlocfilehash: 963ef696e66861f6f67466446e0c1ea19933029e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388308"
---
# <a name="splinestarttype-complextype-visio-xml"></a><span data-ttu-id="65c52-102">SplineStart_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="65c52-102">SplineStart_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="65c52-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="65c52-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65c52-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65c52-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65c52-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="65c52-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65c52-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65c52-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65c52-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="65c52-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65c52-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65c52-109">Definition</span><span class="sxs-lookup"><span data-stu-id="65c52-109">Definition</span></span>

```XML
          <xs:complexType name="SplineStart_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="65c52-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="65c52-110">Elements and attributes</span></span>

<span data-ttu-id="65c52-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="65c52-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65c52-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65c52-112">Child elements</span></span>

|<span data-ttu-id="65c52-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="65c52-113">**Element**</span></span>|<span data-ttu-id="65c52-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="65c52-114">**Type**</span></span>|<span data-ttu-id="65c52-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65c52-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65c52-116">Cell</span><span class="sxs-lookup"><span data-stu-id="65c52-116">Cell</span></span>](cell-element-splinestart-rowvisio-xml.md) <br/> |[<span data-ttu-id="65c52-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="65c52-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="65c52-118">Attributes</span></span>

<span data-ttu-id="65c52-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="65c52-119">None.</span></span>
  

