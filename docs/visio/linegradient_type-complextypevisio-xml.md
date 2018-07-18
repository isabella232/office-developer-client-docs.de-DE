---
title: LineGradient_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 026527ffb6b74ced088bc22ee715be9df1320334
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797311"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="d07d8-102">LineGradient_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d07d8-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d07d8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d07d8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d07d8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d07d8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d07d8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d07d8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d07d8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d07d8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d07d8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d07d8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d07d8-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d07d8-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d07d8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d07d8-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d07d8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d07d8-110">Elements and attributes</span></span>

<span data-ttu-id="d07d8-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d07d8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d07d8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d07d8-112">Child elements</span></span>

|<span data-ttu-id="d07d8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d07d8-113">**Element**</span></span>|<span data-ttu-id="d07d8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d07d8-114">**Type**</span></span>|<span data-ttu-id="d07d8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d07d8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d07d8-116">Row</span><span class="sxs-lookup"><span data-stu-id="d07d8-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d07d8-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="d07d8-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d07d8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="d07d8-118">Attributes</span></span>

<span data-ttu-id="d07d8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d07d8-119">None.</span></span>
  

