---
title: ScratchRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 74f106f34596ca4ff2c200e0127155f4df54da28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391465"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="103a9-102">ScratchRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="103a9-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="103a9-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="103a9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="103a9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="103a9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="103a9-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="103a9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="103a9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="103a9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="103a9-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="103a9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="103a9-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="103a9-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="103a9-109">Definition</span><span class="sxs-lookup"><span data-stu-id="103a9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="103a9-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="103a9-110">Elements and attributes</span></span>

<span data-ttu-id="103a9-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="103a9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="103a9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="103a9-112">Child elements</span></span>

|<span data-ttu-id="103a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="103a9-113">**Element**</span></span>|<span data-ttu-id="103a9-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="103a9-114">**Type**</span></span>|<span data-ttu-id="103a9-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="103a9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="103a9-116">Cell</span><span class="sxs-lookup"><span data-stu-id="103a9-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="103a9-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="103a9-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="103a9-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="103a9-118">Attributes</span></span>

<span data-ttu-id="103a9-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="103a9-119">None.</span></span>
  

