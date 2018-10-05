---
title: ArcTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c30c80eb-6327-ebc3-7ea4-8b2fc7525cc0
ms.openlocfilehash: 73a89d7535a81700a875f68905de844f876a6181
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390149"
---
# <a name="arctotype-complextype-visio-xml"></a><span data-ttu-id="52334-102">ArcTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="52334-102">ArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="52334-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="52334-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52334-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52334-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52334-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="52334-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52334-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="52334-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52334-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="52334-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52334-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="52334-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52334-109">Definition</span><span class="sxs-lookup"><span data-stu-id="52334-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="52334-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="52334-110">Elements and attributes</span></span>

<span data-ttu-id="52334-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="52334-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52334-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52334-112">Child elements</span></span>

|<span data-ttu-id="52334-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="52334-113">**Element**</span></span>|<span data-ttu-id="52334-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="52334-114">**Type**</span></span>|<span data-ttu-id="52334-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52334-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52334-116">Cell</span><span class="sxs-lookup"><span data-stu-id="52334-116">Cell</span></span>](cell-element-arcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="52334-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="52334-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="52334-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="52334-118">Attributes</span></span>

<span data-ttu-id="52334-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="52334-119">None.</span></span>
  

