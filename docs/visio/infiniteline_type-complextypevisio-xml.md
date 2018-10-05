---
title: InfiniteLine_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: f9db3947381da563f2f7d9973d7b2578094d5235
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390373"
---
# <a name="infinitelinetype-complextype-visio-xml"></a><span data-ttu-id="7ce9b-102">InfiniteLine_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7ce9b-102">InfiniteLine_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7ce9b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7ce9b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ce9b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7ce9b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7ce9b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7ce9b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7ce9b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7ce9b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="7ce9b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ce9b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7ce9b-109">Definition</span></span>

```XML
          <xs:complexType name="InfiniteLine_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="7ce9b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7ce9b-110">Elements and attributes</span></span>

<span data-ttu-id="7ce9b-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7ce9b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7ce9b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7ce9b-112">Child elements</span></span>

|<span data-ttu-id="7ce9b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-113">**Element**</span></span>|<span data-ttu-id="7ce9b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-114">**Type**</span></span>|<span data-ttu-id="7ce9b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ce9b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ce9b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="7ce9b-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="7ce9b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7ce9b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7ce9b-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="7ce9b-118">Attributes</span></span>

<span data-ttu-id="7ce9b-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="7ce9b-119">None.</span></span>
  

