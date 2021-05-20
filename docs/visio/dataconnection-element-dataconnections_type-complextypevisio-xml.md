---
title: DataConnection-Element (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrahiert die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer Nicht-XML-Datenquelle.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538403"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="8d9e1-103">DataConnection-Element (DataConnections_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8d9e1-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8d9e1-104">Abstrahiert die Kommunikation zwischen einem oder **mehreren DataRecordset-Elementen** und einer Nicht-XML-Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8d9e1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d9e1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d9e1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8d9e1-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="8d9e1-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8d9e1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8d9e1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8d9e1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8d9e1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8d9e1-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8d9e1-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="8d9e1-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8d9e1-113">Definition</span><span class="sxs-lookup"><span data-stu-id="8d9e1-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8d9e1-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8d9e1-114">Elements and attributes</span></span>

<span data-ttu-id="8d9e1-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8d9e1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d9e1-116">Parent elements</span></span>

|<span data-ttu-id="8d9e1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-117">**Element**</span></span>|<span data-ttu-id="8d9e1-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-118">**Type**</span></span>|<span data-ttu-id="8d9e1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8d9e1-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="8d9e1-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="8d9e1-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="8d9e1-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8d9e1-122">Enthält die **DataConnection-Elemente** für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d9e1-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d9e1-123">Child elements</span></span>

<span data-ttu-id="8d9e1-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d9e1-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d9e1-125">Attributes</span></span>

|<span data-ttu-id="8d9e1-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-126">**Attribute**</span></span>|<span data-ttu-id="8d9e1-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-127">**Type**</span></span>|<span data-ttu-id="8d9e1-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-128">**Required**</span></span>|<span data-ttu-id="8d9e1-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-129">**Description**</span></span>|<span data-ttu-id="8d9e1-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8d9e1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8d9e1-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="8d9e1-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="8d9e1-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8d9e1-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8d9e1-133">Optional</span><span class="sxs-lookup"><span data-stu-id="8d9e1-133">optional</span></span>  <br/> |<span data-ttu-id="8d9e1-134">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-134">The default value is false.</span></span> <span data-ttu-id="8d9e1-135">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="8d9e1-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="8d9e1-136">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-137">Get-Help</span><span class="sxs-lookup"><span data-stu-id="8d9e1-137">Command</span></span>  <br/> |<span data-ttu-id="8d9e1-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8d9e1-138">xsd:string</span></span>  <br/> |<span data-ttu-id="8d9e1-139">Optional</span><span class="sxs-lookup"><span data-stu-id="8d9e1-139">optional</span></span>  <br/> |<span data-ttu-id="8d9e1-140">Die Befehlszeichenfolge, die zum Abfragen der Datenquelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="8d9e1-141">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8d9e1-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="8d9e1-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8d9e1-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8d9e1-144">Optional</span><span class="sxs-lookup"><span data-stu-id="8d9e1-144">optional</span></span>  <br/> |<span data-ttu-id="8d9e1-145">Die Verbindungszeichenfolge, die die parameter definiert, die zum Herstellen einer Verbindung mit einer Datenquelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="8d9e1-146">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-147">FileName</span><span class="sxs-lookup"><span data-stu-id="8d9e1-147">FileName</span></span>  <br/> |<span data-ttu-id="8d9e1-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8d9e1-148">xsd:string</span></span>  <br/> |<span data-ttu-id="8d9e1-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d9e1-149">required</span></span>  <br/> |<span data-ttu-id="8d9e1-150">Der Name der Verbindungsdatei.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-150">The name of the connection file.</span></span> <span data-ttu-id="8d9e1-151">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="8d9e1-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="8d9e1-152">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8d9e1-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="8d9e1-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8d9e1-154">xsd:string</span></span>  <br/> |<span data-ttu-id="8d9e1-155">Optional</span><span class="sxs-lookup"><span data-stu-id="8d9e1-155">optional</span></span>  <br/> |<span data-ttu-id="8d9e1-156">Ein Benutzer hat den Namen für die Datenverbindung angegeben.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="8d9e1-157">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-158">ID</span><span class="sxs-lookup"><span data-stu-id="8d9e1-158">ID</span></span>  <br/> |<span data-ttu-id="8d9e1-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d9e1-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d9e1-160">erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d9e1-160">required</span></span>  <br/> |<span data-ttu-id="8d9e1-161">Die id, die Visio für eine bestimmte Verbindung zugewiesen wird, die innerhalb des Dokuments eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="8d9e1-162">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8d9e1-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="8d9e1-163">Timeout</span></span>  <br/> |<span data-ttu-id="8d9e1-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8d9e1-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8d9e1-165">Optional</span><span class="sxs-lookup"><span data-stu-id="8d9e1-165">optional</span></span>  <br/> |<span data-ttu-id="8d9e1-166">Die Wartezeit in Minuten beim Versuch, eine Verbindung herzustellen, bevor der Versuch beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="8d9e1-167">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

