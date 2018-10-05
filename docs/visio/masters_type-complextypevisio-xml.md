---
title: Masters_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398493"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="7970b-102">Masters_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7970b-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7970b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7970b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7970b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7970b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7970b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7970b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7970b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7970b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7970b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7970b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7970b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7970b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7970b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7970b-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7970b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7970b-110">Elements and attributes</span></span>

<span data-ttu-id="7970b-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7970b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7970b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7970b-112">Child elements</span></span>

|<span data-ttu-id="7970b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7970b-113">**Element**</span></span>|<span data-ttu-id="7970b-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7970b-114">**Type**</span></span>|<span data-ttu-id="7970b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7970b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7970b-116">Master</span><span class="sxs-lookup"><span data-stu-id="7970b-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7970b-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="7970b-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7970b-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="7970b-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7970b-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="7970b-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7970b-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="7970b-120">Attributes</span></span>

<span data-ttu-id="7970b-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="7970b-121">None.</span></span>
  

