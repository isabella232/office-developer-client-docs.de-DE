---
title: MoveTo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: f3c3ba2bfc789661f57c3d21634b5c876bc11f44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393908"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="df249-102">MoveTo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="df249-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="df249-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="df249-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df249-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="df249-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="df249-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="df249-105">**Schema file**</span></span> <br/> |<span data-ttu-id="df249-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="df249-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="df249-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="df249-107">**Extension base**</span></span> <br/> |<span data-ttu-id="df249-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="df249-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df249-109">Definition</span><span class="sxs-lookup"><span data-stu-id="df249-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="df249-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="df249-110">Elements and attributes</span></span>

<span data-ttu-id="df249-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="df249-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="df249-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df249-112">Child elements</span></span>

|<span data-ttu-id="df249-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="df249-113">**Element**</span></span>|<span data-ttu-id="df249-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="df249-114">**Type**</span></span>|<span data-ttu-id="df249-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df249-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df249-116">Cell</span><span class="sxs-lookup"><span data-stu-id="df249-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="df249-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="df249-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="df249-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="df249-118">Attributes</span></span>

<span data-ttu-id="df249-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="df249-119">None.</span></span>
  

