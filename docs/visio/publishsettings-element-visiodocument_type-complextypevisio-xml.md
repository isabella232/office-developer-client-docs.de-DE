---
title: PublishSettings-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Gibt die Einstellungen an, die beim Öffnen des Diagramms mithilfe von Visio Services in Microsoft SharePoint Server 2013 verwendet werden.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541358"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="7912e-103">PublishSettings-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7912e-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7912e-104">Gibt die Einstellungen an, die beim Öffnen des Diagramms mithilfe von Visio Services in Microsoft SharePoint Server 2013 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7912e-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7912e-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7912e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7912e-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7912e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7912e-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7912e-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7912e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7912e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7912e-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7912e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7912e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7912e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7912e-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="7912e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7912e-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="7912e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7912e-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7912e-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7912e-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7912e-114">Elements and attributes</span></span>

<span data-ttu-id="7912e-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7912e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7912e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7912e-116">Parent elements</span></span>

|<span data-ttu-id="7912e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7912e-117">**Element**</span></span>|<span data-ttu-id="7912e-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7912e-118">**Type**</span></span>|<span data-ttu-id="7912e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7912e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7912e-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7912e-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7912e-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7912e-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7912e-122">Gibt Die Eigenschaften einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="7912e-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7912e-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7912e-123">Child elements</span></span>

|<span data-ttu-id="7912e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7912e-124">**Element**</span></span>|<span data-ttu-id="7912e-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7912e-125">**Type**</span></span>|<span data-ttu-id="7912e-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7912e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7912e-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="7912e-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7912e-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="7912e-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7912e-129">Gibt an, ob ein Zeichenblatt im Browser mithilfe von Visio angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7912e-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="7912e-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="7912e-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7912e-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="7912e-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7912e-132">Gibt an, ob ein Recordset mithilfe von Visio aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7912e-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7912e-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="7912e-133">Attributes</span></span>

<span data-ttu-id="7912e-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="7912e-134">None.</span></span>
  

