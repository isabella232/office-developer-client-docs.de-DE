---
title: RowDef_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 11acab820fe51b6dde9cf9d57977699ca3c977cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394587"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="32137-102">RowDef_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="32137-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="32137-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="32137-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32137-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="32137-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="32137-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="32137-105">**Schema file**</span></span> <br/> |<span data-ttu-id="32137-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="32137-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="32137-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="32137-107">**Extension base**</span></span> <br/> |<span data-ttu-id="32137-108">Keine</span><span class="sxs-lookup"><span data-stu-id="32137-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32137-109">Definition</span><span class="sxs-lookup"><span data-stu-id="32137-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32137-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="32137-110">Elements and attributes</span></span>

<span data-ttu-id="32137-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="32137-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="32137-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32137-112">Child elements</span></span>

|<span data-ttu-id="32137-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="32137-113">**Element**</span></span>|<span data-ttu-id="32137-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="32137-114">**Type**</span></span>|<span data-ttu-id="32137-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32137-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32137-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="32137-116">CellDef</span></span> <br/> |[<span data-ttu-id="32137-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="32137-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="32137-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="32137-118">Attributes</span></span>

<span data-ttu-id="32137-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="32137-119">None.</span></span>
  

