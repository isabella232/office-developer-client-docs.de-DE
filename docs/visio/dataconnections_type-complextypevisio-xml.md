---
title: DataConnections_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796786"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="7c577-102">DataConnections_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7c577-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7c577-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7c577-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c577-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c577-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c577-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7c577-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c577-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7c577-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c577-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7c577-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c577-108">Keine</span><span class="sxs-lookup"><span data-stu-id="7c577-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c577-109">Definition</span><span class="sxs-lookup"><span data-stu-id="7c577-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c577-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7c577-110">Elements and attributes</span></span>

<span data-ttu-id="7c577-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7c577-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c577-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c577-112">Child elements</span></span>

|<span data-ttu-id="7c577-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c577-113">**Element**</span></span>|<span data-ttu-id="7c577-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7c577-114">**Type**</span></span>|<span data-ttu-id="7c577-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c577-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c577-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="7c577-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c577-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="7c577-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7c577-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="7c577-118">Attributes</span></span>

|<span data-ttu-id="7c577-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7c577-119">**Attribute**</span></span>|<span data-ttu-id="7c577-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7c577-120">**Type**</span></span>|<span data-ttu-id="7c577-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7c577-121">**Required**</span></span>|<span data-ttu-id="7c577-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c577-122">**Description**</span></span>|<span data-ttu-id="7c577-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7c577-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c577-124">NextID</span><span class="sxs-lookup"><span data-stu-id="7c577-124">NextID</span></span>  <br/> |<span data-ttu-id="7c577-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c577-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c577-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7c577-126">required</span></span>  <br/> ||<span data-ttu-id="7c577-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c577-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

