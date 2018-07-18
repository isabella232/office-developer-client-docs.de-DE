---
title: FillGradientRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40c88316-4710-b5b4-7be4-e3047474d519
ms.openlocfilehash: 4506c7b313ffbbce67aedbad98db7a78ce42ceaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797019"
---
# <a name="fillgradientrowtype-complextype-visio-xml"></a><span data-ttu-id="e90cc-102">FillGradientRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e90cc-102">FillGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e90cc-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="e90cc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e90cc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e90cc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e90cc-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e90cc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e90cc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e90cc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e90cc-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="e90cc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e90cc-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e90cc-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e90cc-109">Definition</span><span class="sxs-lookup"><span data-stu-id="e90cc-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradientRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e90cc-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e90cc-110">Elements and attributes</span></span>

<span data-ttu-id="e90cc-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e90cc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e90cc-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e90cc-112">Child elements</span></span>

|<span data-ttu-id="e90cc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e90cc-113">**Element**</span></span>|<span data-ttu-id="e90cc-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e90cc-114">**Type**</span></span>|<span data-ttu-id="e90cc-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e90cc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e90cc-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e90cc-116">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e90cc-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e90cc-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e90cc-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="e90cc-118">Attributes</span></span>

<span data-ttu-id="e90cc-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e90cc-119">None.</span></span>
  

