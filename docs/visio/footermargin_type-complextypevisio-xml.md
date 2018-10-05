---
title: FooterMargin_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398934"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="f3f83-102">FooterMargin_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f3f83-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f3f83-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f3f83-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3f83-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3f83-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f3f83-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f3f83-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f3f83-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f3f83-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f3f83-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f3f83-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f3f83-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="f3f83-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3f83-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f3f83-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3f83-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f3f83-110">Elements and attributes</span></span>

<span data-ttu-id="f3f83-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f3f83-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f3f83-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3f83-112">Child elements</span></span>

<span data-ttu-id="f3f83-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3f83-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3f83-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3f83-114">Attributes</span></span>

|<span data-ttu-id="f3f83-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f3f83-115">**Attribute**</span></span>|<span data-ttu-id="f3f83-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f3f83-116">**Type**</span></span>|<span data-ttu-id="f3f83-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f3f83-117">**Required**</span></span>|<span data-ttu-id="f3f83-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3f83-118">**Description**</span></span>|<span data-ttu-id="f3f83-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f3f83-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3f83-120">Einheit</span><span class="sxs-lookup"><span data-stu-id="f3f83-120">Unit</span></span>  <br/> |<span data-ttu-id="f3f83-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f3f83-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f3f83-122">Optional</span><span class="sxs-lookup"><span data-stu-id="f3f83-122">optional</span></span>  <br/> ||<span data-ttu-id="f3f83-123">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f3f83-123">Values of the xsd:string type.</span></span>  <br/> |
   

