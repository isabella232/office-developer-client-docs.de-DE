---
title: PublishedPage-Element (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Gibt an, ob ein Zeichenblatt im Browser mithilfe von Visio Services in Microsoft SharePoint Server 2013 angezeigt werden kann.
ms.openlocfilehash: 614c01f12b9a7525620704e5417a106e8703c983
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538375"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a><span data-ttu-id="10b71-103">PublishedPage-Element (PublishSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="10b71-103">PublishedPage element (PublishSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="10b71-104">Gibt an, ob ein Zeichenblatt im Browser mithilfe von Visio Services in Microsoft SharePoint Server 2013 angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="10b71-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10b71-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="10b71-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10b71-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="10b71-106">**Element type**</span></span> <br/> |[<span data-ttu-id="10b71-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="10b71-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="10b71-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10b71-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="10b71-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="10b71-109">**Schema file**</span></span> <br/> |<span data-ttu-id="10b71-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="10b71-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="10b71-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="10b71-111">**Document parts**</span></span> <br/> |<span data-ttu-id="10b71-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="10b71-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10b71-113">Definition</span><span class="sxs-lookup"><span data-stu-id="10b71-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10b71-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="10b71-114">Elements and attributes</span></span>

<span data-ttu-id="10b71-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="10b71-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="10b71-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10b71-116">Parent elements</span></span>

|<span data-ttu-id="10b71-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="10b71-117">**Element**</span></span>|<span data-ttu-id="10b71-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="10b71-118">**Type**</span></span>|<span data-ttu-id="10b71-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10b71-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10b71-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="10b71-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10b71-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="10b71-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10b71-122">Gibt die Einstellungen an, die beim Öffnen des Diagramms mithilfe von Visio werden.</span><span class="sxs-lookup"><span data-stu-id="10b71-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="10b71-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10b71-123">Child elements</span></span>

<span data-ttu-id="10b71-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="10b71-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10b71-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="10b71-125">Attributes</span></span>

|<span data-ttu-id="10b71-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="10b71-126">**Attribute**</span></span>|<span data-ttu-id="10b71-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="10b71-127">**Type**</span></span>|<span data-ttu-id="10b71-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="10b71-128">**Required**</span></span>|<span data-ttu-id="10b71-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10b71-129">**Description**</span></span>|<span data-ttu-id="10b71-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="10b71-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10b71-131">ID</span><span class="sxs-lookup"><span data-stu-id="10b71-131">ID</span></span>  <br/> |<span data-ttu-id="10b71-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10b71-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10b71-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="10b71-133">required</span></span>  <br/> |<span data-ttu-id="10b71-134">Der Bezeichner eines Zeichenblatts.</span><span class="sxs-lookup"><span data-stu-id="10b71-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="10b71-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="10b71-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

