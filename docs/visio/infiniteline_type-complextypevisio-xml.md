---
title: InfiniteLine_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: ec0fb78e01afe0d16d959e100a93d053f96bc559
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542415"
---
# <a name="infiniteline_type-complextype-visio-xml"></a><span data-ttu-id="11f11-102">InfiniteLine_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="11f11-102">InfiniteLine_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="11f11-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="11f11-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11f11-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11f11-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11f11-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="11f11-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11f11-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="11f11-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11f11-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="11f11-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11f11-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="11f11-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11f11-109">Definition</span><span class="sxs-lookup"><span data-stu-id="11f11-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="11f11-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="11f11-110">Elements and attributes</span></span>

<span data-ttu-id="11f11-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="11f11-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11f11-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11f11-112">Child elements</span></span>

|<span data-ttu-id="11f11-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="11f11-113">**Element**</span></span>|<span data-ttu-id="11f11-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="11f11-114">**Type**</span></span>|<span data-ttu-id="11f11-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11f11-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11f11-116">Cell</span><span class="sxs-lookup"><span data-stu-id="11f11-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="11f11-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="11f11-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="11f11-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="11f11-118">Attributes</span></span>

<span data-ttu-id="11f11-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="11f11-119">None.</span></span>
  

