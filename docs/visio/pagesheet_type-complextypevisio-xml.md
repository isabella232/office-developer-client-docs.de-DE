---
title: PageSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797594"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="ade44-102">PageSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ade44-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ade44-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ade44-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ade44-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ade44-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ade44-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ade44-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ade44-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ade44-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ade44-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ade44-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ade44-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="ade44-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ade44-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ade44-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ade44-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ade44-110">Elements and attributes</span></span>

<span data-ttu-id="ade44-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ade44-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ade44-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ade44-112">Child elements</span></span>

<span data-ttu-id="ade44-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ade44-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ade44-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ade44-114">Attributes</span></span>

|<span data-ttu-id="ade44-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ade44-115">**Attribute**</span></span>|<span data-ttu-id="ade44-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ade44-116">**Type**</span></span>|<span data-ttu-id="ade44-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ade44-117">**Required**</span></span>|<span data-ttu-id="ade44-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ade44-118">**Description**</span></span>|<span data-ttu-id="ade44-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ade44-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ade44-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ade44-120">UniqueID</span></span>  <br/> |<span data-ttu-id="ade44-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ade44-121">xsd:string</span></span>  <br/> |<span data-ttu-id="ade44-122">Optional</span><span class="sxs-lookup"><span data-stu-id="ade44-122">optional</span></span>  <br/> ||<span data-ttu-id="ade44-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ade44-123">Values of the xsd:string type.</span></span>  <br/> |
   

