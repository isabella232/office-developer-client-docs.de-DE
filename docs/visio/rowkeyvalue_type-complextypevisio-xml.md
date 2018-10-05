---
title: RowKeyValue_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: 512675538aa17415fa44684613dcd635fe23857f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387685"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="adf7e-102">RowKeyValue_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="adf7e-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="adf7e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="adf7e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adf7e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="adf7e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="adf7e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="adf7e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="adf7e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="adf7e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="adf7e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="adf7e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="adf7e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="adf7e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="adf7e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="adf7e-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="adf7e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="adf7e-110">Elements and attributes</span></span>

<span data-ttu-id="adf7e-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="adf7e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="adf7e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="adf7e-112">Child elements</span></span>

<span data-ttu-id="adf7e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="adf7e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="adf7e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="adf7e-114">Attributes</span></span>

|<span data-ttu-id="adf7e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="adf7e-115">**Attribute**</span></span>|<span data-ttu-id="adf7e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="adf7e-116">**Type**</span></span>|<span data-ttu-id="adf7e-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="adf7e-117">**Required**</span></span>|<span data-ttu-id="adf7e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="adf7e-118">**Description**</span></span>|<span data-ttu-id="adf7e-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="adf7e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="adf7e-120">RowID</span><span class="sxs-lookup"><span data-stu-id="adf7e-120">RowID</span></span>  <br/> |<span data-ttu-id="adf7e-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="adf7e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="adf7e-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="adf7e-122">required</span></span>  <br/> ||<span data-ttu-id="adf7e-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="adf7e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="adf7e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="adf7e-124">Value</span></span>  <br/> |<span data-ttu-id="adf7e-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="adf7e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="adf7e-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="adf7e-126">required</span></span>  <br/> ||<span data-ttu-id="adf7e-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="adf7e-127">Values of the xsd:string type.</span></span>  <br/> |
   

