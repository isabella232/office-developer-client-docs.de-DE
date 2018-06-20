---
title: ScratchRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 2de91fa81bd18b08edb61b52392bc5d06a261884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797982"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="981ec-102">ScratchRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="981ec-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="981ec-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="981ec-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="981ec-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="981ec-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="981ec-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="981ec-105">**Schema file**</span></span> <br/> |<span data-ttu-id="981ec-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="981ec-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="981ec-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="981ec-107">**Extension base**</span></span> <br/> |<span data-ttu-id="981ec-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="981ec-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="981ec-109">Definition</span><span class="sxs-lookup"><span data-stu-id="981ec-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="981ec-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="981ec-110">Elements and attributes</span></span>

<span data-ttu-id="981ec-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="981ec-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="981ec-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="981ec-112">Child elements</span></span>

|<span data-ttu-id="981ec-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="981ec-113">**Element**</span></span>|<span data-ttu-id="981ec-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="981ec-114">**Type**</span></span>|<span data-ttu-id="981ec-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="981ec-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="981ec-116">Cell</span><span class="sxs-lookup"><span data-stu-id="981ec-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="981ec-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="981ec-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="981ec-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="981ec-118">Attributes</span></span>

<span data-ttu-id="981ec-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="981ec-119">None.</span></span>
  

