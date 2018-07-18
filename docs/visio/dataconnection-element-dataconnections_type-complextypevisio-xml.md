---
title: DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Fasst die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer nicht auf XML basierenden Datenquelle zusammen.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796797"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="876f6-103">DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="876f6-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="876f6-104">Fasst die Kommunikation zwischen einem oder mehreren **DataRecordset** -Elementen und einer nicht auf XML basierenden Datenquelle zusammen.</span><span class="sxs-lookup"><span data-stu-id="876f6-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="876f6-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="876f6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="876f6-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="876f6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="876f6-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="876f6-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="876f6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="876f6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="876f6-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="876f6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="876f6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="876f6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="876f6-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="876f6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="876f6-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="876f6-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="876f6-113">Definition</span><span class="sxs-lookup"><span data-stu-id="876f6-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="876f6-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="876f6-114">Elements and attributes</span></span>

<span data-ttu-id="876f6-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="876f6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="876f6-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="876f6-116">Parent elements</span></span>

|<span data-ttu-id="876f6-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="876f6-117">**Element**</span></span>|<span data-ttu-id="876f6-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="876f6-118">**Type**</span></span>|<span data-ttu-id="876f6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="876f6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="876f6-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="876f6-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="876f6-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="876f6-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="876f6-122">Enthält die **DataConnection** -Elemente für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="876f6-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="876f6-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="876f6-123">Child elements</span></span>

<span data-ttu-id="876f6-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="876f6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="876f6-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="876f6-125">Attributes</span></span>

|<span data-ttu-id="876f6-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="876f6-126">**Attribute**</span></span>|<span data-ttu-id="876f6-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="876f6-127">**Type**</span></span>|<span data-ttu-id="876f6-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="876f6-128">**Required**</span></span>|<span data-ttu-id="876f6-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="876f6-129">**Description**</span></span>|<span data-ttu-id="876f6-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="876f6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="876f6-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="876f6-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="876f6-132">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="876f6-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="876f6-133">Optional</span><span class="sxs-lookup"><span data-stu-id="876f6-133">optional</span></span>  <br/> |<span data-ttu-id="876f6-134">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="876f6-134">The default value is false.</span></span> <span data-ttu-id="876f6-135">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="876f6-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="876f6-136">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="876f6-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="876f6-137">Command</span><span class="sxs-lookup"><span data-stu-id="876f6-137">Command</span></span>  <br/> |<span data-ttu-id="876f6-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="876f6-138">xsd:string</span></span>  <br/> |<span data-ttu-id="876f6-139">Optional</span><span class="sxs-lookup"><span data-stu-id="876f6-139">optional</span></span>  <br/> |<span data-ttu-id="876f6-140">Die Befehlszeichenfolge wird zum Abfragen der Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="876f6-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="876f6-141">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="876f6-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="876f6-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="876f6-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="876f6-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="876f6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="876f6-144">Optional</span><span class="sxs-lookup"><span data-stu-id="876f6-144">optional</span></span>  <br/> |<span data-ttu-id="876f6-145">Die Verbindungszeichenfolge, die die Verbindung zu einer Datenquelle erforderlichen Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="876f6-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="876f6-146">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="876f6-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="876f6-147">FileName</span><span class="sxs-lookup"><span data-stu-id="876f6-147">FileName</span></span>  <br/> |<span data-ttu-id="876f6-148">XSD: String</span><span class="sxs-lookup"><span data-stu-id="876f6-148">xsd:string</span></span>  <br/> |<span data-ttu-id="876f6-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="876f6-149">required</span></span>  <br/> |<span data-ttu-id="876f6-150">Der Name der Verbindungsdatei.</span><span class="sxs-lookup"><span data-stu-id="876f6-150">The name of the connection file.</span></span> <span data-ttu-id="876f6-151">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="876f6-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="876f6-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="876f6-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="876f6-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="876f6-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="876f6-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="876f6-154">xsd:string</span></span>  <br/> |<span data-ttu-id="876f6-155">Optional</span><span class="sxs-lookup"><span data-stu-id="876f6-155">optional</span></span>  <br/> |<span data-ttu-id="876f6-156">Ein Benutzer zur Verfügung gestellten Name für die Datenverbindung.</span><span class="sxs-lookup"><span data-stu-id="876f6-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="876f6-157">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="876f6-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="876f6-158">ID</span><span class="sxs-lookup"><span data-stu-id="876f6-158">ID</span></span>  <br/> |<span data-ttu-id="876f6-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="876f6-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="876f6-160">erforderlich</span><span class="sxs-lookup"><span data-stu-id="876f6-160">required</span></span>  <br/> |<span data-ttu-id="876f6-161">Die ID für eine angegebene Verbindung, die innerhalb des Dokuments eindeutig von Visio zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="876f6-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="876f6-162">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="876f6-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="876f6-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="876f6-163">Timeout</span></span>  <br/> |<span data-ttu-id="876f6-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="876f6-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="876f6-165">Optional</span><span class="sxs-lookup"><span data-stu-id="876f6-165">optional</span></span>  <br/> |<span data-ttu-id="876f6-166">Die Wartezeit in Minuten beim Versuch, bevor der Versuch beendet eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="876f6-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="876f6-167">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="876f6-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

