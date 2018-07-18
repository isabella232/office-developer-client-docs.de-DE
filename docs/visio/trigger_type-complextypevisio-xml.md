---
title: Trigger_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798308"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="bbedf-102">Trigger_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bbedf-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bbedf-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bbedf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbedf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bbedf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bbedf-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bbedf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bbedf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bbedf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bbedf-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bbedf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bbedf-108">Keine</span><span class="sxs-lookup"><span data-stu-id="bbedf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bbedf-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bbedf-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bbedf-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bbedf-110">Elements and attributes</span></span>

<span data-ttu-id="bbedf-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bbedf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bbedf-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bbedf-112">Child elements</span></span>

|<span data-ttu-id="bbedf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bbedf-113">**Element**</span></span>|<span data-ttu-id="bbedf-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bbedf-114">**Type**</span></span>|<span data-ttu-id="bbedf-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbedf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bbedf-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="bbedf-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bbedf-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="bbedf-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bbedf-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="bbedf-118">Attributes</span></span>

|<span data-ttu-id="bbedf-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bbedf-119">**Attribute**</span></span>|<span data-ttu-id="bbedf-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bbedf-120">**Type**</span></span>|<span data-ttu-id="bbedf-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bbedf-121">**Required**</span></span>|<span data-ttu-id="bbedf-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbedf-122">**Description**</span></span>|<span data-ttu-id="bbedf-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bbedf-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bbedf-124">N</span><span class="sxs-lookup"><span data-stu-id="bbedf-124">N</span></span>  <br/> |<span data-ttu-id="bbedf-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bbedf-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bbedf-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bbedf-126">required</span></span>  <br/> ||<span data-ttu-id="bbedf-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bbedf-127">Values of the xsd:string type.</span></span>  <br/> |
   

