---
title: HeaderMargin_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393719"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="26b2b-102">HeaderMargin_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="26b2b-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="26b2b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="26b2b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b2b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26b2b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="26b2b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="26b2b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="26b2b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="26b2b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="26b2b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="26b2b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="26b2b-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="26b2b-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26b2b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="26b2b-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26b2b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="26b2b-110">Elements and attributes</span></span>

<span data-ttu-id="26b2b-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="26b2b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="26b2b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26b2b-112">Child elements</span></span>

<span data-ttu-id="26b2b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="26b2b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26b2b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="26b2b-114">Attributes</span></span>

|<span data-ttu-id="26b2b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="26b2b-115">**Attribute**</span></span>|<span data-ttu-id="26b2b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="26b2b-116">**Type**</span></span>|<span data-ttu-id="26b2b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="26b2b-117">**Required**</span></span>|<span data-ttu-id="26b2b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26b2b-118">**Description**</span></span>|<span data-ttu-id="26b2b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="26b2b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26b2b-120">Einheit</span><span class="sxs-lookup"><span data-stu-id="26b2b-120">Unit</span></span>  <br/> |<span data-ttu-id="26b2b-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="26b2b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="26b2b-122">Optional</span><span class="sxs-lookup"><span data-stu-id="26b2b-122">optional</span></span>  <br/> ||<span data-ttu-id="26b2b-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="26b2b-123">Values of the xsd:string type.</span></span>  <br/> |
   

