---
title: Trigger_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396330"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="75bf5-102">Trigger_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="75bf5-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="75bf5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="75bf5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75bf5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75bf5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="75bf5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="75bf5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="75bf5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="75bf5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="75bf5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="75bf5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="75bf5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="75bf5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75bf5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="75bf5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="75bf5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="75bf5-110">Elements and attributes</span></span>

<span data-ttu-id="75bf5-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="75bf5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75bf5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75bf5-112">Child elements</span></span>

|<span data-ttu-id="75bf5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="75bf5-113">**Element**</span></span>|<span data-ttu-id="75bf5-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="75bf5-114">**Type**</span></span>|<span data-ttu-id="75bf5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75bf5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75bf5-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="75bf5-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75bf5-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="75bf5-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="75bf5-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="75bf5-118">Attributes</span></span>

|<span data-ttu-id="75bf5-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="75bf5-119">**Attribute**</span></span>|<span data-ttu-id="75bf5-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="75bf5-120">**Type**</span></span>|<span data-ttu-id="75bf5-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="75bf5-121">**Required**</span></span>|<span data-ttu-id="75bf5-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75bf5-122">**Description**</span></span>|<span data-ttu-id="75bf5-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="75bf5-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75bf5-124">N</span><span class="sxs-lookup"><span data-stu-id="75bf5-124">N</span></span>  <br/> |<span data-ttu-id="75bf5-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="75bf5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="75bf5-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="75bf5-126">required</span></span>  <br/> ||<span data-ttu-id="75bf5-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="75bf5-127">Values of the xsd:string type.</span></span>  <br/> |
   

