---
title: Character_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: d4145bf92c053f67ed11e827b528e05fd4ffc7f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386600"
---
# <a name="charactertype-complextype-visio-xml"></a><span data-ttu-id="207a6-102">Character_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="207a6-102">Character_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="207a6-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="207a6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="207a6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="207a6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="207a6-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="207a6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="207a6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="207a6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="207a6-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="207a6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="207a6-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="207a6-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="207a6-109">Definition</span><span class="sxs-lookup"><span data-stu-id="207a6-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="207a6-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="207a6-110">Elements and attributes</span></span>

<span data-ttu-id="207a6-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="207a6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="207a6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="207a6-112">Child elements</span></span>

|<span data-ttu-id="207a6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="207a6-113">**Element**</span></span>|<span data-ttu-id="207a6-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="207a6-114">**Type**</span></span>|<span data-ttu-id="207a6-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="207a6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="207a6-116">Row</span><span class="sxs-lookup"><span data-stu-id="207a6-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="207a6-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="207a6-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="207a6-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="207a6-118">Attributes</span></span>

<span data-ttu-id="207a6-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="207a6-119">None.</span></span>
  

