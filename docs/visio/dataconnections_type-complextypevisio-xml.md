---
title: DataConnections_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542457"
---
# <a name="dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="ad86e-102">DataConnections_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ad86e-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ad86e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ad86e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad86e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad86e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad86e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ad86e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad86e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ad86e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad86e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ad86e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad86e-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ad86e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad86e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ad86e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad86e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ad86e-110">Elements and attributes</span></span>

<span data-ttu-id="ad86e-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ad86e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad86e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad86e-112">Child elements</span></span>

|<span data-ttu-id="ad86e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad86e-113">**Element**</span></span>|<span data-ttu-id="ad86e-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad86e-114">**Type**</span></span>|<span data-ttu-id="ad86e-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad86e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad86e-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="ad86e-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad86e-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="ad86e-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad86e-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad86e-118">Attributes</span></span>

|<span data-ttu-id="ad86e-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad86e-119">**Attribute**</span></span>|<span data-ttu-id="ad86e-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad86e-120">**Type**</span></span>|<span data-ttu-id="ad86e-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ad86e-121">**Required**</span></span>|<span data-ttu-id="ad86e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad86e-122">**Description**</span></span>|<span data-ttu-id="ad86e-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ad86e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad86e-124">NextID</span><span class="sxs-lookup"><span data-stu-id="ad86e-124">NextID</span></span>  <br/> |<span data-ttu-id="ad86e-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad86e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad86e-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad86e-126">required</span></span>  <br/> ||<span data-ttu-id="ad86e-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ad86e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

