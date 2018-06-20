---
title: PageContents_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: ab74c646e72a7ebe5fbf5863c196d5b115be9b43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797579"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="5b480-102">PageContents_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="5b480-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5b480-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5b480-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b480-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b480-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5b480-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5b480-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5b480-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5b480-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5b480-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5b480-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5b480-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5b480-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b480-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5b480-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b480-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5b480-110">Elements and attributes</span></span>

<span data-ttu-id="5b480-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5b480-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5b480-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5b480-112">Child elements</span></span>

|<span data-ttu-id="5b480-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b480-113">**Element**</span></span>|<span data-ttu-id="5b480-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5b480-114">**Type**</span></span>|<span data-ttu-id="5b480-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b480-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b480-116">Stellt eine Verbindung her</span><span class="sxs-lookup"><span data-stu-id="5b480-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b480-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="5b480-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b480-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="5b480-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b480-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="5b480-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5b480-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="5b480-120">Attributes</span></span>

<span data-ttu-id="5b480-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="5b480-121">None.</span></span>
  

