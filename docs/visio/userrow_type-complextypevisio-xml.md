---
title: UserRow_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 0d670ecdc9230843cffb0336f3f4ad5c53285615
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798373"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="318dd-102">UserRow_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="318dd-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="318dd-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="318dd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="318dd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="318dd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="318dd-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="318dd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="318dd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="318dd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="318dd-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="318dd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="318dd-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="318dd-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="318dd-109">Definition</span><span class="sxs-lookup"><span data-stu-id="318dd-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="318dd-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="318dd-110">Elements and attributes</span></span>

<span data-ttu-id="318dd-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="318dd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="318dd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="318dd-112">Child elements</span></span>

|<span data-ttu-id="318dd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="318dd-113">**Element**</span></span>|<span data-ttu-id="318dd-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="318dd-114">**Type**</span></span>|<span data-ttu-id="318dd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="318dd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="318dd-116">Cell</span><span class="sxs-lookup"><span data-stu-id="318dd-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="318dd-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="318dd-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="318dd-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="318dd-118">Attributes</span></span>

<span data-ttu-id="318dd-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="318dd-119">None.</span></span>
  

